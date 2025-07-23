# 🎧 Spotify Tracks DWH & Analytics Project

**By Kyrellos El Naggar**  
📅 July 2025

---

## 📌 Project Overview

This project demonstrates a full-stack business intelligence solution built on the **Microsoft BI Stack** (SSIS, SSAS, Power BI), analyzing over **232,000 Spotify tracks** across **26 music genres**.

The goal is to design an end-to-end **Data Warehouse and Analysis System** capable of delivering deep insights into musical data — such as tempo, popularity, energy, danceability, and more.

---

## 🚀 Tech Stack

| Component | Technology |
|----------|-------------|
| ETL      | SQL Server Integration Services (SSIS) |
| DWH      | SQL Server 2019 |
| Cube     | SQL Server Analysis Services (SSAS Tabular) |
| Visualization | Power BI |
| Scripting | T-SQL, DAX |

---

## 🗂️ Data Description

**Source**: Spotify Track Dataset  
**Records**: 232,725 tracks  
**Genres**: 26  
**Key Columns**:
- `track_name`, `artist_name`, `genre`
- `popularity`, `danceability`, `energy`, `acousticness`
- `tempo`, `mode`, `key`, `loudness`, `valence`, `duration_ms`

---

## 📊 Project Layers

### 1️⃣ SSIS – ETL Pipeline

- Extracted data from Excel files
- Cleaned and staged into 3-layer architecture:
  - `ODS_Spotify`
  - `STG_Spotify`
  - `DWH_Spotify`
- Transformed audio metrics and conformed dimensions

🔧 SSIS Packages included:
- `Load_ODS.dtsx`
- `Transform_Staging.dtsx`
- `Load_DWH.dtsx`

---

### 2️⃣ Data Warehouse – Star Schema

**Fact Table**:
- `FactSpotifyTrack` (with popularity, energy, etc.)

**Dimensions**:
- `DimTrack`
- `DimGenre`
- `DimMusicTheory`

Star schema optimized for SSAS and Power BI querying.

---

### 3️⃣ SSAS Tabular Model

- Created KPIs and measures in DAX:
  - Total Tracks, Average Popularity, Danceable Energetic Tracks, High Energy %, Acousticness %, etc.
- Enabled complex slicing/filtering by genre, artist, track metrics

📦 Measures file: `Spotify_SSAS_Model.bim`

---

### 4️⃣ Power BI Dashboard

- Fully interactive report with 4 main tabs:
  - 🎛️ Overview
  - 🎤 Artist Insights
  - 📈 Track Metrics
  - 🎼 Genre Analytics

🎨 Features:
- Dynamic slicers (genre, key, mode)
- KPI cards, clustered visuals, and advanced DAX filters

📊 File: `SpotifyDashboard.pbix`

---

## 📈 Business Impact

This project enables stakeholders to:
- Identify popular and rising artists
- Analyze energy, tempo, and danceability trends
- Segment music by emotional tone and structure
- Build data-driven playlists and recommendations


---

## 📜 License

This project is for academic and demonstration purposes only. Not affiliated with Spotify.


