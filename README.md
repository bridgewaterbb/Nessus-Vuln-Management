<p align="center">
<img src="https://i.imgur.com/YZIYBLv.png" alt="Nessus"/>
</p>

<h1>Vulnerability Scanning and Management with Nessus</h1>
In this lab I scanned a virtual machine for vulnerabilities with Nessus. I then implemented fixes in order to manage the vulnerabilities found.<br />

<h2>Technology Utilized</h2>

- VMware Workstation Pro (Virtual Machine)
- Nessus Essentials Vulnerability Scanner
- Windows Command Line

<h2>Operating Systems</h2>

- Windows 10

<h2>Overview</h2>

- Download Nessus onto host OS.
- Download and install VMware Workstation. Download Windows 10 image and create virtual machine.
- Ensure network connectivity between host and virtual machine.
- Configure VM machine's registry to allow for Nessus scans.
- Run scans from Nessus of virtual machine under different circumstances.
- Remediate vulnerabilities.

<h2>Set up</h2>

<p>
<img src="https://i.imgur.com/OP9UpKZ.png" height="80%" width="80%" alt="Dashboard"/>
</p>
<p>
I installed VMware Workstation Pro onto my host machine. I then downloaded a Windows 10 image and created a virtual machine in VMware. I also downloaded Nessus and completed this installation. After the Windows 10 install I ensured there was network connectivity between my host machine and the virtual machine. For simplicity, I disabled the Firewall on the virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/35wLjIk.png" height="80%" width="80%" alt="Scan 1"/>
</p>
<p>
I added the virtual machine's IPv4 address to the target list in the Nessus dashboard. In order to see the most complete scans I enabled remote registry on the Windows machine and ensured file and printer sharing was turned on. I then configured the registry to allow it to be scanned by Nessus. 
</p>
<br />

<h2>Scanning</h2>

<p>
<img src="https://i.imgur.com/7ZFFvrQ.png" height="80%" width="80%" alt="Scan 2"/>
</p>
<p>
I ran a scan of the Windows virtual machine without credentials and observed the results. I then performed a credentialed scan of the virtual machine and observed more results of varying levels of severity. 
</p>
<br />

<p>
<img src="https://i.imgur.com/xD4Sk9m.png" height="80%" width="80%" alt="Scan 3"/>
</p>
<p>
I then intentionally installed a deprecated version of Firefox onto the virtual machine. Another credentialed scan was completed and I observed the change in results. There were obviously many more in this scan. Additionally, there were more critical vulnerabilities in this scan. 
</p>
<br />

<p>
<img src="https://i.imgur.com/vSajdAC.png" height="80%" width="80%" alt="Vulns"/>
</p>
<p>
In order to remediate many of the vulnerabilities found by Nessus I uninstalled Firefox and updated Windows 10 to its latest version. 
</p>
<br />

