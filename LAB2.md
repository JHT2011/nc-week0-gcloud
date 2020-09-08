# LAB 2: Setup GCloud SDK  and Create VM using gcloud command

# Cài đặt và cấu hình google cloud sdk

## Refer:
```
https://cloud.google.com/sdk/docs/quickstart-debian-ubuntu
```

## Step 1: Tạo một Google Cloud Project

## Step 2: Cài đặt google cloud sdk trên ubuntu >= 16.04
```
# Add the Cloud SDK distribution URI as a package source
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] http://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

# Import the Google Cloud public key
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -

# Update the package list and install the Cloud SDK
sudo apt-get update && sudo apt-get install google-cloud-sdk
```

## Init
* gcloud init


## GCloud Commands:
* List config: gcloud config list
* Set/update config: 
* List:
	```
	# List instance
	gcloud compute instances list
	# List zone
	gcloud compute zones list
	# List image
	gcloud compute images list
	```

* Create instance: 
	```
	gcloud compute instances create ncdevop02 --zone=asia-southeast1-a --tags=ncdevops02 --image-family=centos-7 --image-project centos-cloud --machine-type=e2-small 
	```

## SSH lên server
* SSH len server: gcloud compute ssh <instance-name>
