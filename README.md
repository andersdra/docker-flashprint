# Usage

`docker-compose up`  
`alias flashprint='docker-compose -f /path/to/docker-compose.yml up -d'`

Or when pulled from Docker hub:  

docker run --name flashprint \\  
--cap-drop=ALL \\  
-e DISPLAY \\  
-v /tmp/.X11-unix:/tmp/.X11-unix:ro \\  
-v $PWD/3d_files:/3d_files \\  
-v $PWD/flashprint_config:/flashprint/.FlashPrint \\  
andersdra/flashprint

`alias flashprint='docker start flashprint'`


a workfolder named 3d_files will be mounted at /  
config files is stored in ./flashprint_config
