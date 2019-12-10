### Step to build image and running container for DSP classroom in Linux OS

1. Clone this repository to local computer

2. Open folder and build docker image using command in the terminal

   - ***docker build -t dsp:1.9 .***

     <img src="picture/1.png" >

     **note: you can change the name image to the name you want*
     
     **dont forget use . (dot) in the end of command*

3. After finish build the image, than you can running the container following this command

   - ***docker run -it --net=host -v /tmp/.X11-unix:/tmp/.X11-unix --env QT_X11_NO_MITSHM=1 -e DISPLAY --rm dsp:1.9***

     <img src="picture/2.png">
     
     explanation of command:
     
     - *-it*= connect the container to terminal
     - *--net=host* = use network from local 
     - *-e DISPLAY*= export display server from local computer
     - *--rm* = remove the container when stop
     
     

4. Than it will show the result like picture bellow this.

   <img src="picture/5.png">

5. Open the **link** on the browser your computer, it will automatically go to your notebook .

   <img src="picture/4.png">

   
   
   <img src="picture/6.png">

### 

- ### If you want to running in windows that have installed WSL ([*Windows Subsystem Linux*](https://docs.microsoft.com/en-us/windows/wsl/install-win10)) you can reference from **[here](https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly)**. Make sure you need to install Xserver for windows, such as [Xming](https://sourceforge.net/projects/xming/), [X410](https://token2shell.com/howto/x410/) and Etc.