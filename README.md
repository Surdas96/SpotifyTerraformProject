# SpotifyTerraformProject
# I have added terraform project guide for reference. 
# Also added below steps and screenshot for reference. 

# Created provider.tf file
![provider](https://github.com/user-attachments/assets/670f17f2-ad05-43cd-aceb-78434fc127dc)

# Created app using spotify developer option https://developer.spotify.com/dashboard/

![Spotify developer app](https://github.com/user-attachments/assets/01cb6d74-9c52-4cc1-ab21-bbeecb747b7b)

# Create environment for client id and secret. create file .env 

![environment](https://github.com/user-attachments/assets/3891141f-1e4b-498d-97e4-83305a58731c)

# we need to run spotify auth proxy as docker container
(Here we are creating docker container which have docker image name - ghcr.io/conradludgate/spotify-auth-proxy:latest
in docker you will see image and container created )
docker run --rm -it -p 27228:27228 --env-file .env ghcr.io/conradludgate/spotify-auth-proxy

![Docker container command](https://github.com/user-attachments/assets/1d2d6779-5641-4784-8423-5bcc5996d695)

![Docker Container](https://github.com/user-attachments/assets/b7edba31-c954-49db-a406-9e90e87f199f)

# create terraform.tfvars file to save variables

![tfvars](https://github.com/user-attachments/assets/2bd8a85d-1c55-4c6e-9281-3233a62d10fd)

# Now call this variable in side variable block. Create variable.tf file 

![variable](https://github.com/user-attachments/assets/3c304483-73ae-444e-a3d9-61d3605f5af7)

# create playlist.tf file

![playlist](https://github.com/user-attachments/assets/7a925c75-d3ed-49b3-862a-3dfe3d23d4a4)


# On terminal run 
-terraform init command
-terraform plan
-terraform apply

# Check spotify account playlist will be added. 

![Spotify playlist](https://github.com/user-attachments/assets/6d254eca-f20e-468e-94d8-cf97e4df2550)


# Finish

