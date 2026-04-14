# IoT Cloud Monitoring System 
### Real-Time Temperature & Humidity Monitoring — AWS 
 
## Deskripsi Proyek 
Sistem monitoring IoT berbasis AWS untuk memantau data suhu dan 
kelembaban 
secara real-time. Data sensor dari simulator Wokwi dikirim via MQTT 
ke AWS IoT 
Core, diproses oleh Lambda, disimpan di RDS & S3, dan ditampilkan di 
dashboard 
web yang berjalan di EC2. 
 
## Arsitektur 
Wokwi Simulator → MQTT → AWS IoT Core → Lambda → RDS MySQL 
                                       ↓ 
                                      S3 (raw payload) 
EC2 (Web Dashboard) ← HTTP ← Browser (End User) 
 
## Layanan AWS yang Digunakan - AWS IoT Core  : MQTT broker & rule engine - AWS Lambda    : Serverless data processing - AWS RDS MySQL : Structured sensor data storage - AWS S3        : Raw payload object storage - AWS EC2       : Web server & monitoring dashboard 
 
## Cara Menjalankan 
# 1. Clone repository 
git clone https://github.com/<org>/iot-cloud-monitoring.git 
 
# 2. Setup infrastruktur (Minggu 2) 
cd infra/ && terraform init && terraform plan && terraform apply 
 
# 3. Deploy Lambda (Minggu 3) 
cd lambda/ && pip install -r requirements.txt && ./deploy.sh 
 
# 4. Jalankan Wokwi Simulator 
# Buka wokwi.com → load project → start simulation 
 
## Tim Pengembang 
| Role               | Nama               | NIM           | 
|--------------------|---------------     |-------------  | 
| Cloud Architect    | Agung Setyo Pambudi| 2330205030060 | 
| DevOps Engineer    | Muhamad Rafliansyah| 2330205030043 | 
| Backend Developer  | Septio Praja       | 2330205030045 | 
| Security Engineer  | Agung Setyo Pambudi| 2330205030060 | 
 
## Lisensi: MIT | Platform: AWS ap-southeast-1 (Singapore) 
