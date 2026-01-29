# 🏗️ Sediver ITSM Dashboard

**Interactive Project Management Dashboard** for Sediver Freshservice ITSM Implementation.

Built following **ITIL 4** methodology and best practices from **Freshservice** implementation guides.

---

## 🚀 Features

### 📊 Activity Matrix
- Editable task status (Non Iniziato, In Corso, Completato, Bloccato)
- Inline date editing (Start/End)
- Phase filtering (Assessment, Design, Build, UAT, Go-Live)
- Owner filtering (CRMP, Client, Joint)
- Search functionality

### 📅 Interactive GANTT Chart
- D3.js powered visualization
- Dependencies arrows
- Critical path highlighting (red border)
- Milestone diamonds
- Today line indicator
- Hover tooltips with task details

### ⚡ Critical Path Monitor
- Automatic critical path calculation
- Real-time impact analysis
- Milestone mapping
- Duration tracking

### ⚠️ Risk Register
- Probability × Impact matrix visualization
- Click-through risk details
- Linked tasks identification
- Mitigation & contingency tracking

### 📈 Phase Progress
- Visual progress bars per ITSM phase
- Date range indicators
- Completion percentage

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| HTML5 | Structure |
| CSS3 | Styling (no framework) |
| JavaScript | Logic |
| D3.js v7 | GANTT visualization |
| Chart.js | Overview charts |
| localStorage | Data persistence |

---

## 📁 Project Structure

```
sediver-dashboard/
├── index.html              # Main dashboard
├── css/
│   └── styles.css          # All styles
├── js/
│   ├── app.js              # Core logic & state
│   ├── dashboard.js        # UI rendering
│   └── gantt.js            # D3 GANTT chart
└── data/
    ├── sediver-project.json # Project tasks & milestones
    └── sediver-risks.json   # Risk register
```

---

## 🌐 GitHub Pages Deployment

1. Create a new repository on GitHub
2. Upload all files maintaining the folder structure
3. Go to **Settings → Pages**
4. Select **main** branch and **/ (root)** folder
5. Save and wait for deployment

Your dashboard will be available at:
```
https://<username>.github.io/<repository-name>/
```

---

## 💾 Data Persistence

All changes are automatically saved to **localStorage**:
- Task status updates
- Date modifications
- Risk status changes

To reset to original data, click the **🔄 Reset** button.

To export current state, click **📥 Esporta** for JSON download.

---

## 🎨 Customization

### Adding Tasks
Edit `data/sediver-project.json`:
```json
{
  "id": "T054",
  "name": "New Task Name",
  "phase": "Phase Group",
  "itsmPhase": "build",
  "priority": "Alta",
  "owner": "CRMP",
  "status": "Non Iniziato",
  "startDate": "2026-04-01",
  "endDate": "2026-04-15",
  "milestone": false,
  "dependencies": ["T053"],
  "critical": false
}
```

### Adding Risks
Edit `data/sediver-risks.json`:
```json
{
  "id": "R011",
  "name": "Risk Name",
  "description": "Risk description",
  "category": "Technical",
  "probability": "Media",
  "impact": "Alto",
  "score": 6,
  "status": "Aperto",
  "linkedTasks": ["T001", "T002"],
  "mitigation": "Mitigation plan",
  "contingency": "Contingency plan"
}
```

---

## 📋 ITSM Phases

| Phase | Color | Description |
|-------|-------|-------------|
| Assessment | 🔵 Blue | Requirements gathering, AS-IS/TO-BE |
| Design | 🟢 Green | Configuration design, SLA definition |
| Build | 🟠 Orange | Implementation, workflows, integrations |
| UAT | 🟣 Purple | User acceptance testing |
| Go-Live | 🔴 Red | Production deployment |
| Hypercare | 🩵 Teal | Post-launch support |

---

## 📝 License

Proprietary - CRMpartners © 2026

---

## 🤝 Support

For questions about Freshservice implementation:
- [Freshservice Documentation](https://support.freshservice.com/)
- [ITIL 4 Foundation](https://www.axelos.com/certifications/itil-service-management)
