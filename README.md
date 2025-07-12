#  N8N Rain Alert Agent

> An automated agent built using **n8n** that alerts you via **Gmail** if rain is forecasted in your location between **9:00 AM and 12:00 PM**, optionally checking your **Google Calendar** to only notify you on days you’re scheduled to go out.

---

## Features

-  Scheduled to run daily at **9:00 AM**
- Optionally checks your **Google Calendar** for any events between **9:30 AM and 12:00 PM**
- Uses the **OpenWeatherMap API** to get forecasted weather data
- Sends a **Gmail email notification** if rain is expected during that window
- Smart logic using n8n’s **Switch** and **If** nodes
- Secure API key and credential usage
- Fully customizable and self-hostable

---

## Workflow Overview

<img width="1583" height="597" alt="rain alert" src="https://github.com/user-attachments/assets/92ebba08-48cc-4563-a461-0e284b439305" />


---

##  APIs & Services Used

| Service         | Purpose                         |
| --------------- | ------------------------------- | 
| OpenWeatherMap  | Fetch hourly forecast data      | 
| Google Calendar | Check for scheduled events      | 
| Gmail API       | Send email alerts               |
| n8n             | Workflow orchestration platform |

---

##  Setup Instructions

### 1. Clone & Install n8n (Self-hosted)

> You can also use n8n cloud or Docker version.

```bash
git clone https://github.com/BhaveshBhakta/N8N-Rain-Alert-Agent.git
cd N8N-Rain-Alert-Agent
```

### 2. Get Your API Keys

#### OpenWeatherMap

* Go to: [https://openweathermap.org/api](https://openweathermap.org/api)
* Sign up and get your API Key

####  Gmail API

* Go to: [https://console.cloud.google.com](https://console.cloud.google.com)
* Enable **Gmail API**
* Create **OAuth 2.0 credentials**

#### Google Calendar API

* Enable **Calendar API** in the same project
* Reuse the same OAuth credentials

---

##  Customization

| Element            | You Can Change                      |
| ------------------ | ----------------------------------- |
| Location (lat/lon) | Adjust to your city / coordinates   |
| Time Window        | Change from 9:00–12:00 to any range |
| Notification Type  | Use Telegram, Slack, Discord, etc.  |
| Trigger Time       | Run check earlier/later if needed   |

---

## Testing

* Add a mock event in your Google Calendar
* Modify the weather API node to return test data if needed
* Run the workflow manually to debug flow

---


## Future Improvements

* Dynamic location detection via IP
* Telegram/WhatsApp notifications
* Rain intensity thresholds (e.g., >5mm only)
* Store logs to Google Sheets

---

## 📄 License

This project is open-source and free to use under the [MIT License](https://opensource.org/licenses/MIT).
