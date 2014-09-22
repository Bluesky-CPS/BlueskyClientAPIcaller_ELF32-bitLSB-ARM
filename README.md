BlueskyClientAPIcaller_ELF32-bitLSB-ARM
========================================
 Here is a client API caller(Demo version 1) of Blue-sky server binary execution for ELF32bit ARM such as Raspbian kernel. You can clone it and copy to executionable directory. (Cuation: It is not support for Private API now.)

 **For example (Linux):**

  ```shell 
   #!/bin/sh
   
   sudo cp SKYBLUECLIENT /usr/bin/.
   
   sudo chmod 777 /usr/bin/SKYBLUECLIENT

   edIP="Your RaspberryPI IP address."

   GPIO_PIN_NUMBER_OF_YOUR_DEFINE="3"

   BLUESKYSERVER="127.0.0.1:8189"

   SKYBLUECLIENT -c "http://${BLUESKYSERVER}" -s "sensornetwork ${edIP} set d ${GPIO_PIN_NUMBER_OF_YOUR_DEFINE} 1"

   SKYBLUECLIENT -c "http://${BLUESKYSERVER}" -s "sensornetwork ${edIP} get d ${GPIO_PIN_NUMBER_OF_YOUR_DEFINE}"

   SKYBLUECLIENT -c "http://${BLUESKYSERVER}" -s "sensornetwork ${edIP} set d ${GPIO_PIN_NUMBER_OF_YOUR_DEFINE} 0"
  
  ```
