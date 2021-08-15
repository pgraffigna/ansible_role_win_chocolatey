# ansible_role_win_chocolatey

Playbook para automatizar la instalación de herramientas que uso en un sistema windows.

---
roles:
- choco_instalar
- choco_desinstalar
- choco_paquetes

---
scripts:
- ConfigureRemotingForAnsible.ps1
- Windows10DebloaterGUI.ps1 --> para eliminar la telemetria + bloatware de los equipos con Windows10

---
Descargar y ejecutar:
- powershell.exe -exec bypass -C "wget -Uri 'https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1' -OutFile winrm.ps1; ./winrm"

---
fix:
- no module name "winrm"
- sudo apt install -y python3-winrm && pip install "pywinrm>=0.2.2"


