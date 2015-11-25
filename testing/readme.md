### Template sandbox ###

The templates in this folder are being tested and may or may not work

### vmss-docker-simple.json ###

Deploy a simple Ubuntu/Docker scale set.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgbowerman%2Fazure-myriad%2Fmaster%2Ftesting%2Fvmss-docker-simple.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<br/><br/>

### vmss-ubuntu-autoscale.json ###

Deploy a simple Linux based scale set.

How to use:
- Deploy with an instance count of 1.
- SSH into port 50000 and max the CPU.
- After a few minutes additional VMs will be created.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgbowerman%2Fazure-myriad%2Fmaster%2Fautoscale%2Fvmss-ubuntu-autoscale.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<br/><br/>

### vmss-lap-autoscale.json ###

Simple self-contained Ubuntu/Apache/PHP autoscale & load balancing example. Scale Set scales up when avg CPU across all VMs > 60%, scales down when avg CPU < 50%.

- Deploy the scale set with an instance count of 1 
- After it is deployed look at the resource group public IP address resource (in portal or resources explorer). Get the IP or domain name.
- Browse to the website (port 80), which shows the current backend VM name.
- Hit the "Do work" button with an iteration count of say 300 (represents seconds of max CPU).
- After a few minutes the scale set capacity will increase, and refreshing the browser and going to the home page a few times will show additional backend VM name(s).
- You can increase the work by connecting to more backend websites, or decrease by letting the iterations time-out, in which case the scale set will scale down � hence after about 10 minutes the capacity should be back down to 1.


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgbowerman%2Fazure-myriad%2Fmaster%2Fautoscale%2Fvmss-lap-autoscale.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>