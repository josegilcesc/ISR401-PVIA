### Manifiesto de evidencias privadas — PFC Entrega 1

Las evidencias originales (carta de aceptación firmada, registros de contacto, audios, consentimientos firmados) **no se publican** en este repositorio porque contienen datos personales de terceros (LOPDP). Conforme a la sección 5 del formulario de consentimiento PFC-ISR401-POSIA-A03, los formularios firmados y las grabaciones originales se guardan dentro de un archivo cifrado cuya contraseña solo conoce el docente responsable, en la carpeta institucional restringida del equipo (cuenta @uteq.edu.ec). Las transcripciones anonimizadas se guardan en la misma carpeta, fuera del archivo cifrado. El material identificable se conserva como máximo 24 meses desde el cierre del periodo académico.

Este manifiesto registra cada archivo privado para que su integridad pueda verificarse con su huella SHA-256.

#### Cómo calcular la huella
En PowerShell:
```powershell
Get-FileHash .\nombre-del-archivo.pdf -Algorithm SHA256
```

#### Registro
| N.º | Archivo (carpeta privada) | Tipo de evidencia | Fecha | Duración | SHA-256 | Registrado por |
| :--- | :--- | :--- | :---: | :---: | :--- | :--- |
| E-01 | E-01_carta-aceptacion.pdf | Carta de aceptación firmada por la organización | 18/11/2026 | — | `F2BF8E0BEF29BD80521D38A638B2F61A6D8286C38FDEE8A8DBCC60298A0778AD` | José Gilces |
| E-02 | E-02_primer-contacto.pdf | Registro del primer contacto con la organización | 17/11/2026 | — | `E8E8F438027EF236AAA88E1E5156DFB6D3265C036F52C51F5E178CB2ACAD542F` | José Gilces |
| E-03 | ACTA-ELI-CAJ-01_consentimiento.pdf | Consentimiento informado firmado — ACTA-ELI-CAJ-01 | 19/11/2026 | — | `EA2D19C7798990E4494A98696B67E4EB3FB4A0174E84776E9C1415EB42962A5B` | Allan Mendoza |
| E-04 | ACTA-ELI-CAJ-01_audio.m4a | Audio de entrevista — ACTA-ELI-CAJ-01 (cajera-vendedora con experiencia, SH-01) | 19/11/2026 | 16 min | `463834B979B2CFA489609A1791F768510CB99C322998AA3A9904506A28C1B5BD` | Allan Mendoza |
| E-05 | ACTA-ELI-CAJ-01_transcripcion.pdf | Transcripción anonimizada — ACTA-ELI-CAJ-01 | 19/11/2026 | — | `6D7DEE2FD877136EA70905F8388B3C40B8075C5B07662C976A6AFFE7CF1BB7AF` | Allan Mendoza |
| E-06 | ACTA-ELI-CAJ-02_consentimiento.pdf | Consentimiento informado firmado — ACTA-ELI-CAJ-02 | 19/11/2026 | — | `0EA109657FC6D41F01B4B266034CFCC65C221C478631E4F0E054D2F1A299B9C6` | Winston Cedeño |
| E-07 | ACTA-ELI-CAJ-02_audio.m4a | Audio de entrevista — ACTA-ELI-CAJ-02 (vendedor nuevo, SH-04) | 19/11/2026 | 13 min | `0A51D8D58550A61DF7686D0B3277594098DB288E73C9474DA0C66C56ED074946` | Winston Cedeño |
| E-08 | ACTA-ELI-CAJ-02_transcripcion.pdf | Transcripción anonimizada — ACTA-ELI-CAJ-02 | 19/11/2026 | — | `01B86480681DD548980243A9BA3DC4D949A20E34B227A9582909461625994B7E` | Winston Cedeño |
| E-09 | ACTA-ELI-ADM-01_consentimiento.pdf | Consentimiento informado firmado — ACTA-ELI-ADM-01 | 19/11/2026 | — | `C2885509BC950E85A70DE20C572DA973714FD7F909D6BB9158FE1FE6A636000A` | José Gilces |
| E-10 | ACTA-ELI-ADM-01_audio.m4a | Audio de entrevista — ACTA-ELI-ADM-01 (propietario, SH-03) | 19/11/2026 | 31 min | `78DA2670506A6B8B4567012AE80E76E1181BA57D5E6D9A4C843AF67A4B80CE42` | José Gilces |
| E-11 | ACTA-ELI-ADM-01_transcripcion.pdf | Transcripción anonimizada — ACTA-ELI-ADM-01 | 19/11/2026 | — | `BC950FA11FF7FF0984506B8CAA36B3DC02C1FA48A1D535B3B8CC87385D150988` | José Gilces |
| E-12 | PFC-E1_evidencias_cifradas.7z | Archivo cifrado con E-01, E-03, E-04, E-06, E-07, E-09 y E-10 | 20/11/2026 | — | `88D866CFACF8AA60C1D264729E347D6F79117BD78B42B7466BC9B439C107032C` | José Gilces |

Equivalencia con los códigos de trabajo usados durante el levantamiento: ENV-01 = ACTA-ELI-CAJ-01, ENV-02 = ACTA-ELI-CAJ-02, ENV-03 = ACTA-ELI-ADM-01.

Notas:
* La duración de E-10 corresponde a la versión final editada (31 min) tras recortar el fragmento previo al inicio formal de la sesión y el consentimiento.
* La huella SHA-256 se calcula sobre la versión final de cada archivo, antes de empaquetarlo dentro del archivo cifrado.
* El correo de contacto solicitado al cierre de ACTA-ELI-CAJ-01 no está cubierto por la autorización e) del formulario (solo teléfono); se eliminó del registro público.
