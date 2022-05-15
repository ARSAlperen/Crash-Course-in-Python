
## Disk Usage and CPU Usage

The shutil module offers a number of high-level operations on files and collections of files. In particular, it provides functions that support file copying and removal. It comes under Python's standard utility modules. disk_usage() method is used to get disk usage statistics of the given path. This method returns a named tuple with the attributes total, used, and free. The total attribute represents the total amount of space, the used attribute represents the amount of used space, and the free attribute represents the amount of available space, in bytes.

psutil (Python system and process utilities) is a cross-platform library for retrieving information on the processes currently running and system utilization (CPU, memory, disks, network, sensors) in Python. It's useful mainly for system monitoring, profiling, limiting process resources, and managing running processes. cpu_percent() returns a float showing the current system-wide CPU use as a percentage. When the interval is 0.0 or None (default), the function compares process times to system CPU times elapsed since the last call, returning immediately (non-blocking). That means that the first time it's called it will return a meaningful 0.0 value. When the interval is > 0.0, the function compares process times to system CPU times elapsed before and after the interval (blocking).


      import shutil as s
      import psutil


      def check_disk_usage(disk):
          usage=s.disk_usage(disk)
          free=usage.free/usage.total*100 #free disk space
          return free>20

      def check_cpu_usage():
          usage=psutil.cpu_percent(1)  # cpu usage percent(interval)
          return usage<75

      if not check_disk_usage("/") or not check_cpu_usage():
          print("ERROR!")
      else:
          print("OK")

![image](https://user-images.githubusercontent.com/105153770/168491439-7d5f4bbf-de7c-4ce4-95ed-6c96d8b3989c.png)

## Virtual Machine and Qwiklabs
A virtual machine, or VM, is a computer simulated through software. It simulates all the necessary hardware to the operating system that's running inside the machine.

# QwikLabs

## Fix File Permissions

navigate to the scripts directory

      cd scripts

List the files to find the script
            
      ls

To view the contents of this file

      cat health_checks.py
      
This script begins with a line containing the #! character combination, which is commonly called hash bang or shebang and continues with the path to the interpreter.

      #!/usr/bin/env python3

run the Python file

      ./health_checks.py
      
add execute permission to the file

     sudo chmod +x health_checks.py

Use a nano editor to open the file health_checks.py.

      nano health_checks.py
      
And once the changes are done, save the file by clicking Ctrl-o, enter key and Ctrl-x.

Use nano editor to create a new file network.py:

      nano network.py
      
network.py code

      #!/usr/bin/env python3

      import requests
      import socket

      def check_localhost():
              localhost=socket.gethostbyname('localhost')
              if localhost=="127.0.0.1":
                      return True


      def check_connectivity():
              request=requests.get("http://www.google.com")

              if request.status_code==200:
                      return True

      check_localhost()
      check_connectivity()

