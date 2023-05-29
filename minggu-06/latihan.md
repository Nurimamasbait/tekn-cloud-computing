# 1.INSTAL GO, MYSQL DAN MONGODB  
### Instal Go
1. Buka file go yang telah didownload, kemudian klik dan klik run

![img](foto6/2.1.png)

2. selanjutnya klik next

![img](foto6/22.png)

3. klik next

![img](foto6/23.png)

4. Selanjutnya memilih folder yang ingin anda letakan file Go yang akan diinstal

![img](foto6/24.png)

5. Selanjutnya klik Install

![img](foto6/25.png)

6. Kemudian tunggu sampai proses install selesai

![img](foto6/26.png)

7. Dan setelah selesai klik Finish

![img](foto6/27.png)

8. Setelah terinstal , buka cmd untuk melihat apakah Go sudah terinstal

![img](foto6/go.png)

### Install MYSQL
Jika anda telah install mysql anda dapat melihat perintah untuk melihat version mysql

![img](foto6/01.png)

### Install MongoDB
1. Klik file MongoDB yang telah didownload

![img](foto6/3.png)

2. Selanjutnya klik next

![img](foto6/4.png)

3. Lanjut Next

![img](foto6/5.png)

4. Selanjutnya akan menampilkan Servir Configuration
Pada bagian ini akan di perlihatkan lokasi datanya , bias dilihat pada tanda

![img](foto6/6.png)

5. Hilangkan tanda Install MongoDB Compass dan klik nxt

![img](foto6/7.png)

6. Selanjutnya klik Install

![img](foto6/8.png)

7. Kemudian tunggu proses install selesai

![img](foto6/9.png)

8. Setelah installan selesai maka Finish , setelah itu klik finish

![img](foto6/10.png)

9. Selanjutnya buka Folder MongoDB, kemudian klik mongoDB.exe

![img](foto6/11.png)

10. Maka tampilan mongoDB jika telah seperti di bawah ini maka telah berasil terinstall
![img](foto6/12.png)

# 2. 2 contoh program Go masing-masing untuk koneksi dan membaca data dari MySQL dan MongoDB

## Program Go koneksi MYSQL

1. Buat file main.go


Jalankan file dengan perintah go run main.go



2. Buat program file Koneksi MongoDB

Membuat file mongodb.go

package main
import (
	"context"
	"fmt"

	"go.mongodb.org/mongo-driver/bson"
	"go.mongodb.org/mongo-driver/mongo"
	"go.mongodb.org/mongo-driver/mongo/options"
)
func main() {

	// Define the mongodb client URL
	var uri = "mongodb://localhost:27017"

	// Establish the connection
	client, err := mongo.Connect(context.TODO(), options.Client().ApplyURI(uri))
	if err != nil {
		panic(err)
	}

	// Create go routine to defer the closure
	defer func() {
		if err = client.Disconnect(context.TODO()); err != nil {
			panic(err)
		}
	}()

	coll := client.Database("Employee").Collection("scoreCollection")
	docs := []interface{}{
		bson.D{{"name", "Alley"}, {"score", 7.5}},
		bson.D{{"name", "Bob"}, {"score", 8.5}},
		bson.D{{"name", "Carry"}, {"score", 6.8}},
		bson.D{{"name", "Daniel"}, {"score", 5.5}},
		bson.D{{"name", "Danish"}, {"score", 4.8}},
		bson.D{{"name", "Era"}, {"score", 9.2}},
		bson.D{{"name", "Hush"}, {"score", 10}},
		bson.D{{"name", "Halley"}, {"score", 3.6}},
		bson.D{{"name", "John"}, {"score", 7.5}},
	}
	// insertMany
	result, err := coll.InsertMany(context.TODO(), docs)
	if err != nil {
		panic(err)
	}
	// end insertMany

	// When you run this file, it should print:
	// Document inserted with ID: ObjectID("...")
	for _, id := range result.InsertedIDs {
		fmt.Printf("\t%s\n", id)
	}
}

