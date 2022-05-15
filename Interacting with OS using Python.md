
## Disk Usage and CPU Usage

      import shutil as s

      usage=s.disk_usage("/")
      print(usage)

      print(usage.free/usage.total*100) #free disk space

      import psutil

      psutil.cpu_percent(0.1)
