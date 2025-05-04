# **SIA Updater**
**Company:** AHMSA  
**Version:** V1 – May 2025  
**Type:** Windows Background Application  
**Category:** System Integration Utility  

---

## 🧭 Overview  
**SIA Updater** is a Windows application built in **C#** and **SQL Server** using **Visual Studio**, designed to automatically monitor and process updates to the **SIA system** by syncing contract-related data extracted from SAP TXT files.  

It runs as a background service, regularly scanning a designated folder for new files and executing the parsing and database update logic without user interaction.

---

## 💡 Idea & Concept  
To eliminate manual intervention and ensure that **SIA modules**—including **Warehouse**, **Petty Cash**, and **Material Testing**—always operate with up-to-date contract information, this utility was developed to automate data import from SAP TXT files.

---

## ✨ Features & Functionality  
- **Background Sync Engine:** Monitors folders for new TXT files  
- **Data Parser:** Reads, validates, and formats SAP TXT data  
- **Auto Contract Sync:** Creates or updates contract entries in the SIA database  
- **Silent Execution:** Runs with minimal footprint, invisible to most users  
- **Execution Log:** Tracks updates, errors, skipped files, and update timestamps  
- **Always-On Design:** Runs at intervals or continuously depending on configuration  
- **Multi-threaded Handling:** Optimized for file scanning and DB writes  

---

## ⚙️ Tech Stack  
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)  
![.NET Framework](https://img.shields.io/badge/.NET%20Framework-512BD4?style=for-the-badge&logo=dotnet)  
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver)  
![Visual Studio](https://img.shields.io/badge/IDE-Visual%20Studio-5C2D91?style=for-the-badge&logo=visualstudio)  

---

## 🏗 Architecture & Design  
- File system watcher monitors designated directory  
- TXT parser extracts structured data  
- SQL commands handle upserts into `Contracts` and related tables  
- Logs execution to a dedicated table for audits  
- Configurable schedule via Windows Task Scheduler or app settings  

---

## 🚀 Installation & Setup  
**Prerequisites:**  
- Windows OS  
- .NET Framework  
- SQL Server with access to SIA DB  
- Folder with SAP TXT export feed  

**Setup Steps:**  
1. Configure folder path and DB credentials  
2. Schedule using Task Scheduler or set up as a Windows Service  
3. Monitor logs in the DB or log file

---

## 🧑‍💻 My Role & Contributions  
- 🛠 Built entire application architecture and scheduling system  
- 🧪 Designed and tested file parser for SAP TXT format  
- 🧱 Developed database integration logic and logging tools  
- 🔄 Integrated updater logic with existing SIA modules  

---

## 🧗 Challenges & Learnings  
- Ensuring fault-tolerant file processing without duplicates  
- Handling malformed or partial SAP exports gracefully  
- Achieving reliable execution in long-running unattended environments  
- Providing feedback loops for failed entries  

---

## 📈 Future Enhancements  
- Add real-time alert system for failed updates  
- UI tool for admins to manually trigger or override updates  
- Support CSV format as fallback or future standard  
- Visual reporting of weekly contract update activity  

---

## 🔗 Related Projects  
- [SIA – Main Platform](../SIA.md)  
- [SIA – Tests of Materials Module](../SIA-Tests-of-Materials.md)  
- [SIA – Petty Cash Module](../SIA-Petty-Cash.md)  

---

## 🪪 License  
**Internal Project – AHMSA**  
All rights reserved. Not available for public contribution or commercial use.