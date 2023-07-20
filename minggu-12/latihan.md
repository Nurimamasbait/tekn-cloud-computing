# Kubernetes
## Instal Minikuber

Menggunakan perintah ini:PowerShell

![img](foto/1/1.png)

![img](foto/1/2.png)

Selanjutnya tambahkan biner ke file .

Pastikan untuk menjalankan PowerShell sebagai Administrator.minikube.exePATH

![img](foto/1/3.png)

## Instal kubectl binary with curl di Windows

Perintah ini:curl

![img](foto/2/12.png)

Validasi biner terhadap file checksum:kubectl
Menggunakan Command Prompt untuk membandingkan output secara manual dengan file checksum yang diunduh:CertUtil

![img](foto/2/22.png)

Menggunakan PowerShell untuk mengotomatiskan verifikasi menggunakan operator untuk Dapatkan hasil OR

![img](foto/2/23.png)

Perintah Memvalidasi biner (opsional)
Unduh file checksum:kubectl

![img](foto/2/24.png)

Uji untuk memastikan versi sama dengan yang diunduh:kubectl

![img](foto/2/25.png)

Atau gunakan ini untuk tampilan versi yang terperinci:

![img](foto/2/26.png)

Setelah install Minikuber dan kubectl ,selanjutnya membuat minikube cluster

## Create a minikube cluster

![img](foto/01.png)

## Open the Kubernetes dashboard

![img](foto/04.png)

## Create a Deployment

![img](foto/05.png)

View the Deployment:

![img](foto/07.png)

View the Pod:

![img](foto/08.png)

View cluster events

![img](foto/09.png)

View the kubectl configuration

![img](foto/10.png)

## Create a Service

![img](foto/11.png)

View the Service you created:

![img](foto/12.png)

Run the following command:

![img](foto/13.png)

Hasil 

![img](foto/13a.png)

## Enable addons

List the currently supported addons:

![img](foto/14.png)

Enable an addon, for example, metrics-server:

![img](foto/15.png)

View the Pod and Service you created by installing that addon:

![img](foto/16.png)

Disable metrics-server:

![img](foto/17.png)

## Clean up

Now you can clean up the resources you created in your cluster:

![img](foto/18.png)

Stop the Minikube cluster

![img](foto/19.png)








