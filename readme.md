# On Host Pi      
  ## Install TigerVNC     
    ```
    sudo apt-get install tigervnc-standalone-server
    ```  
  ## Edit the VNC config  
  
    ```
    sudo nano  ~/.vnc/xstartup
    ```   
    
  #### add the following two lines to the end and save the file  
    
    ```  
    cd ~/KlipperScreen    
    exec ~/.KlipperScreen-env/bin/python ~/KlipperScreen/screen.py    
    ```       
  ## Create Xsession config file     
    ```sudo nano .Xsession```  
    
  #### add the following and save     
    
    ```xsetroot -solid grey -cursor_name left_ptr```     

  ## Launch VNC service    
  
    ```vncserver :5 -geometry 320x240 -interface {your ip address} -localhost=0```     
