+++ 
draft = false
date = 2022-09-26T20:16:43+02:00
title = "Powershell"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

# PowerShell

---

#### Creacion de usuarios Directorio Activo

```powershell

foreach($usuario in Get-Content .\usuarios.txt)
{
    $usuario
    $password = (ConvertTo-SecureString "Alum4dos" -AsPlainText -force)
    New-ADUSer -Name $usuario -Sam $usuario -Path "OU=asir1,OU=alumnos,DC=andel,DC=local" -AccountPassword $password -Enable $true
}

```

#### Creacion de formulario para creacion de usuarios

```powershell

using assembly System.Windows.Forms
using namespace System.Windows.Forms
 
class Operacion
{ 
  [Int]$operacion
  [String]$nombre
 
    #Constructor de la clase
    Operacion($operacion,$nombre)
    {
        $this.operacion = $operacion
        $this.nombre = $nombre
    }
}
 
# Crear array de objetos Operacion
$arrayoperaciones = New-Object System.Collections.ArrayList
 
$form = [Form] @{
 Text = 'Mi formulario'
}
 
$TextBox = [TextBox] @{
 Location = New-Object System.Drawing.Size(100,80)
}

$TextBox = [TextBox] @{
 Location = New-Object System.Drawing.Size(100,120)
}

$button = [Button] @{
 Text = 'Pulsar'
 Location = New-Object System.Drawing.Size(100,180)
}
$button.add_Click{
 Write-Host $TextBox.Text
 $arrayoperaciones.add([Operacion]::new(1,$TextBox.Text))
}
 
$form.Controls.Add($TextBox)
$form.Controls.Add($TextBox2)
$form.Controls.Add($button)
$form.ShowDialog()
$arrayoperaciones | ConvertTo-Json | Out-File operacion.txt -Append -Encoding default

```

#### Sacar el hash de los procesos en ejecución

```powershell

foreach($proceso in Get-Process | select path)
{

    Get-FileHash ($proceso).path

}

```