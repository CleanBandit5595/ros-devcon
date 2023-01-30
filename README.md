# ROS Dev-Container Base

## Porpuse
This project is a base for deploying a ROS devcontainer in an offline environment.


## First-time setup
To use the project in an offline environment we must build the base-image online!

To build the base image run the following:
```
git clone 
cd base-image
docker build . -t ros-dev-base:latest
```

To save the new image locally run:
```
cd ..
docker image save ros-dev-base:latest -o ros-dev-base.tar
```

## VSCode Extentions
This project aleady have some useful extentions for the vs-server.
To add new exentions, download all the `.vsix` files and place them at `.devcontainer/vs-ext` folder.
Open `.devcontainer.json` file and add the following line for each extention:
```
{
    # ...
    "extentions": [
        # ...
        "${localWorkspaceFolder}/vs-ext/NAME_OF_EXT_FILE"
    ]
}
```

## Moving offline
Copy this repo folder with the base-image to a USB drive and move it to the offline environment.
Once the files are present offline navigate in to the folder and run:
```
docker load ros-dev-base.tar
```

That's it!
You can now launch the `.devcontainer` in the vs-code as a remote vs-server