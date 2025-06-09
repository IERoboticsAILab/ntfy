# 🔔 ntfy.sh stack

This lab setup uses [`ntfy.sh`](https://ntfy.sh), a simple HTTP-based pub-sub notification service, to send real-time alerts and messages. This guide explains how to use `ntfy.sh` to send and receive notifications.

---

## 📦 What is `ntfy.sh`?

`ntfy.sh` lets you **send push notifications** to your phone or desktop using simple HTTP requests or CLI commands. It's great for lab alerts, build systems, monitoring, or custom scripts.

---

## ✅ Getting Started

### Creating a topic

Click this button on the user interface:
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/a7e63f33-b5c3-43d2-accd-aec3aa067589" />

And enter your topic's name here, which will create the appropriate route on the API:
<img width="755" alt="image" src="https://github.com/user-attachments/assets/65e05278-8906-4b88-bc38-837a1440c152" />


---

### 📡 Subscribe to a Topic

Each notification topic is just a name. Subscribe by visiting:

```
http://10.205.10.2:1337/<your-topic>
```

You can bookmark that URL or open it in a browser tab to receive real-time updates.

Or install the [ntfy mobile app](https://ntfy.sh/app/) and subscribe to the same topic name.

There is are official Python and JavaScript Libraries to interface with these, feel free to check them out as well.

---

### 📤 Send a Notification

You can publish a message by simply sending a poset request to the URL with your topic, this can be done with whatever technology you prefer, but for testing purposes you can try this command:

```bash
curl -d "Hi" 10.205.10.2:1337/alerts

```

---

Let me know if you'd like to tailor this README to a specific lab workflow (e.g., integration with cron jobs, sensors, Python scripts, etc.).
