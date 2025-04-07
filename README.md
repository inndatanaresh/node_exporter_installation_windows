# Install Node Exporter (windows_exporter) using .msi on Windows

1. Download the .msi File using the below link

   # https://github.com/prometheus-community/windows_exporter/releases/download/v0.30.6/windows_exporter-0.30.6-amd64.msi

2. Install the .msi

   # It installs by default to:
     C:\Program Files\windows_exporter

   # It installs and runs the windows_exporter as a Windows Service

3. Check Service is Running

   # Press Win + R, type services.msc, and hit Enter
   # Find windows_exporter in the list
   # Make sure Status is Running

4. Open Firewall Port 9182 (Optional)

   # powershellCopyEditNew-NetFirewallRule -DisplayName "windows_exporter" -Direction Inbound -LocalPort 9182 -Protocol TCP -Action Allow

5. Test in Browser

   # http://<Windows-IP>:9182/metrics 

