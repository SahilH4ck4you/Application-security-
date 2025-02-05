### To learn Docker PenTesting
https://attackdefense.pentesteracademy.com/listingnoauth?labtype=container-security-miscellaneous&subtype=container-security-miscellaneous-tools


### To perform Docker PenTesting
1. Find Docker User on https://hub.docker.com/
2. Extract all images
3. Run Trufflehog on Docker Images:- ```trufflehog docker --image <user>/<image> | tee <image>.txt```
4. Analyse the Results Manually

#### To get Shell in Docker Image
```sudo docker run --rm -it --entrypoint=/bin/bash <user>/<image>```
