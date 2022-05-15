
## Disk Usage and CPU Usage


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
