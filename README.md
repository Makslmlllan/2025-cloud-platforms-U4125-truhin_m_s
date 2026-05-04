# 2025-cloud-platforms-U4125-truhin_m_s
# Cloud Platforms (2025–2026)

## ITMO University  
Faculty: FTMI  
Course: Cloud Platforms  
Group: U4125  
Student: Trukhin Maksim  


About the repository

The course covers:
- Google Cloud Platform (GCP)
- Cloud infrastructure basics
- Virtual machines and storage
- Access management (IAM)
- Practical cloud service usage


Repository structure
├── lab1/
│ ├── Lab1.md
│ └── images/
├── README.md
├── LICENSE
└── .gitignore


Lab 1 — Google Cloud Overview

Тема:  
Overview of Google Cloud and basic services

Что сделал:
- Created Service Account with IAM roles
- Created Virtual Machine (Compute Engine)
- Worked with Cloud Storage (gsutil)
- Copied files from bucket to VM
- Analyzed access rights and IAM behavior

## Ход работы

Шаг 1. Получение доступа к Google Cloud

Шаг 2. Создание Service Account

В разделе **IAM & Admin → Service Accounts** был создан сервисный аккаунт:

- Name: mtrukhin-sa-lab1

Сервисному аккаунту была назначена роль:

- Storage Admin

Это дало полный доступ к Cloud Storage.


Шаг 3. Создание виртуальной машины

В разделе Compute Engine → VM instances была создана виртуальная машина со следующими параметрами:

- Name: mtrukhin-vm-lab1
- Machine type: e2-micro
- Provisioning model: Spot

<img width="1710" height="1107" alt="Снимок экрана 2026-05-04 в 18 26 15" src="https://github.com/user-attachments/assets/2332b419-9e24-403f-9c89-3364f7ac1610" />

Шаг 4. Подключение к виртуальной машине

Подключение к VM было выполнено через SSH-интерфейс Google Cloud.
<img width="1710" height="1107" alt="Снимок экрана 2026-05-04 в 18 28 19" src="https://github.com/user-attachments/assets/f9322305-ff3f-4c13-a774-e36671f94912" />

Шаг 5. Работа с Cloud Storage

Просмотр содержимого bucket

Была выполнена команда:

```bash
gsutil ls gs://lab1-bucket-itmo
Была создана локальная директория
Файлы были скопированы

<img width="1710" height="1107" alt="Снимок экрана 2026-05-04 в 18 29 55" src="https://github.com/user-attachments/assets/8d5b9f9b-2501-4b09-be20-f7d25e93f22b" />

Шаг 6. Проверка используемого 

По команде: gcloud auth list
Результат показал, что VM использует default Compute Engine service account: 307056602443-compute@developer.gserviceaccount.com

Шаг 7. Изменение ролей доступа
Storage Admin → Compute Viewer

<img width="1710" height="1107" alt="Снимок экрана 2026-05-04 в 18 32 14" src="https://github.com/user-attachments/assets/b345e905-3f65-47c5-992a-102ddd0bc018" />
Шаг 8. Очистка ресурсов

<img width="1710" height="1107" alt="Снимок экрана 2026-05-04 в 18 26 15" src="https://github.com/user-attachments/assets/5f6ccf7b-1ccb-45ad-a518-040e1cd7f277" />



<img width="1710" height="1107" alt="Снимок экрана 2026-05-04 в 18 33 55" src="https://github.com/user-attachments/assets/30a86c8b-d026-4915-87e4-41e95a06e65b" />

После завершения работы:

Виртуальная машина была удалена
Service Account может быть удалён при необходимости

Technologies used

- Google Cloud Platform (GCP)
- Compute Engine
- Cloud Storage
- IAM (Identity and Access Management)
- gcloud CLI
- gsutil


Автор

Trukhin Maksim 
ITMO University  
