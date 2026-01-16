# HeartOxy

A comprehensive health monitoring application for Apple Watch and iPhone that provides 24/7 heart rate and SpO2 monitoring with intelligent alerts, emergency notifications, and detailed health analytics.

## Features

### Apple Watch App
- **24/7 Continuous Monitoring**: Real-time heart rate and SpO2 tracking
- **Threshold Alerts**: Customizable warning and critical alerts for abnormal readings
- **Rapid Repeat Critical Alerts**: 10-second repeating notifications for critical violations
- **Real-time iPhone Sync**: Live data sync to iPhone

### iPhone App
- **Enhanced Live Chart**: Real-time scrolling chart with smooth animations and live ticker
- **Historical Data Visualization**: Beautiful charts showing trends over time
- **Time Range Selection**: View data in multiple time windows (30m, 1h, 3h, 6h, 12h, 24h)
- **HealthKit Import**: Import historical heart rate and SpO2 data from Apple Health
- **CSV Export**: Export all health data with timestamps in ddMMyyyy HH:mm:ss format
- **Alert History**: Complete violation records with historical tracking
- **Emergency SOS Integration**: Quick access to Apple's native Emergency SOS
- **Watch Connectivity**: Real-time and queued data sync from Apple Watch

### Alert System
- **Multi-Tier Delivery**: Watch local notifications, WatchConnectivity, CloudKit emergency alerts
- **Normal Alerts**: 60-second cooldown for warning threshold violations
- **Critical Alerts**: 10-second rapid repeat notifications (no limit) for critical violations
- **Dismiss All Action**: Long-press notification to clear all pending and delivered alerts


---

## Requirements

### Hardware

| Device | Minimum | SpO2 Support |
|--------|---------|--------------|
| **Apple Watch** | Series 4 | Series 6+ required for SpO2 |
| **iPhone** | iPhone 8 | All supported |

### Software

| Platform | Minimum Version |
|----------|-----------------|
| **watchOS** | 9.0+ |
| **iOS** | 16.0+ |
| **Xcode** | 15.0+ |

### Full SpO2 Functionality
- Apple Watch Series 6, 7, 8, 9, 10
- Apple Watch Ultra, Ultra 2

> **Note:** Apple Watch Series 4, 5, and SE models support heart rate monitoring only. SpO2 readings will show as unavailable.

---
