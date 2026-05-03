# 🔍 Audit-AI · Prototip d'Auditoria Intel·ligent

> **Demostració pràctica de com la IA pot automatitzar i millorar el procés d'auditoria comptable.**  
> Desenvolupat com a cas d'ús formatiu per a auditors/es externs interns, controllers i directors/es financers/es (CFO).

---

## 📋 Descripció del projecte

Aquest repositori conté un dossier complet d'auditoria sintètica per a l'empresa fictícia **NordBrix Solutions, S.L.** (distribució de materials de construcció sostenible), corresponent al **tancament de l'exercici 2025** (1 de gener – 31 de desembre de 2025), acompanyat d'un prototip funcional que demostra com la intel·ligència artificial pot analitzar dades comptables i detectar incidències de forma automàtica.

El projecte té tres components principals:

| Component | Format | Descripció |
|-----------|--------|------------|
| Checklist d'auditoria | `.docx` | Control integral de balanç i àrees fiscals (català i castellà) |
| Dossier de dades sintètiques | `.xlsx` | Balanç, P&G, amortitzacions, clients, proveïdors i conciliació bancària |
| Prototip interactiu | `.html` | Aplicació web que simula l'anàlisi IA en temps real |

---

## 🏗️ Estructura del repositori

```
audit-ai/
│
├── docs/
│   ├── Checklist_tancament_auditoria.docx   # Checklist en català
│   │
├── data/
│   └── NordBrix_Dossier_Auditoria_2025.xlsx    # Dossier dades sintètiques
│       ├── Portada
│       ├── 1. Balanç de Situació
│       ├── 2. Compte de P&G
│       ├── 3. Llibre Amortitzacions
│       ├── 4. Llibre de Clients
│       ├── 5. Llibre de Proveïdors
│       └── 6. Conciliació Bancària
│
├── prototype/
│   └── Nordbrix_audit_demo.html                      # Prototip interactiu (demo mode)
│
└── README.md
```

---

## 🚀 Com utilitzar el prototip

### Opció A — Mode demo (sense API key)

Simplement obre el fitxer `prototype/audit_ai_demo.html` al navegador. Les dades de NordBrix ja estan integrades i pots analitzar tots els mòduls sense cap configuració addicional. Ideal per a presentacions i demostracions.

### Opció B — Mode real (amb API key d'Anthropic)

Per connectar el prototip a l'API real de Claude i analitzar els teus propis fitxers:

1. **Obtén una API key** a [console.anthropic.com](https://console.anthropic.com)
   - Crea un compte (gratuït)
   - Apartat **API Keys** → **Create Key**
   - La clau té el format `sk-ant-api03-...`

2. **Obre el prototip** al navegador i introdueix la clau al camp corresponent.

> ⚠️ **Important:** Mai posis la teva API key directament al codi ni la pugis a GitHub.

---

## 📊 Contingut del dossier NordBrix

### Empresa fictícia

**NordBrix Solutions, S.L.** és una empresa de distribució de materials de construcció sostenible (CNAE 4673) amb seu a Barcelona. Totes les dades són **100% fictícies** i han estat generades exclusivament amb finalitats formatives i demostratives.

### Incidències intencionades

El dossier conté **19 incidències** prèviament introduïdes per simular un escenari d'auditoria real:

| Àrea | Incidència | Gravetat | Import |
|------|-----------|----------|--------|
| Balanç | IVA creditor no concilia model 390 | 🔴 Crítica | 1.840 € |
| Balanç | Provisió insolvències +106% sense justificació | 🔴 Crítica | 19.700 € |
| P&G | Tipus efectiu IS: 29,7% vs 25% nominal | 🔴 Crítica | — |
| P&G | Variació existències signe invers vs any anterior | 🟡 Mitjana | 85.520 € |
| Amortitzacions | Quota anti-incendis no registrada al compte 681 | 🔴 Crítica | 2.890 € |
| Amortitzacions | Diferència quadre vs P&G | 🔴 Crítica | 9.800 € |
| Clients | Client C014 en concurs de creditors | 🔴 Crítica | 18.100 € |
| Clients | Client C009 possible fallida (subprovisió) | 🔴 Crítica | 5.600 € |
| Proveïdors | P006 Isover: TMP 112 dies (Llei 15/2010) | 🔴 Crítica | 24.100 € |
| Proveïdors | Operació vinculada potencial Saint-Gobain | 🔴 Crítica | 79.700 € |
| Conciliació | Cobrament duplicat client C007 | 🔴 Crítica | 1.191,64 € |
| Conciliació | Diferència residual no quadrada | 🟡 Mitjana | 120,21 € |
| Conciliació | Ingrés de 1.000 € sense identificar | 🟡 Mitjana | 1.000 € |

**Impacte total estimat sobre el resultat net declarat (67.420 €): –15.400 € (–22,8%)**

---

## 🛠️ Tecnologies utilitzades

- **Frontend:** HTML5 · CSS3 · JavaScript (vanilla, sense dependències)
- **IA:** [Anthropic Claude API](https://docs.anthropic.com) (`claude-sonnet-4-20250514`) amb streaming SSE
- **Documents:** Python · `openpyxl` (Excel) · `docx-js` (Word)
- **Fonts:** IBM Plex Mono · Fraunces (Google Fonts)

---

## 🎯 Casos d'ús demostrats

- **Auditor extern:** detecció automàtica d'incidències i classificació per gravetat (crítica / mitjana / informativa)
- **Auditor intern:** monitoratge continu de desviacions sense revisió manual full per full
- **Director financer (CFO):** visió executiva agregada amb impacte quantificat sobre el resultat
- **Formació:** entorn segur per practicar tècniques d'auditoria sobre dades fictícies realistes

---

## ⚖️ Avís legal

> Les dades contingudes en el dossier Excel (NordBrix Solutions, S.L., CIF B-08319274, adreces, imports, noms de clients i proveïdors) són **completament fictícies**. Qualsevol coincidència amb persones físiques o jurídiques reals és purament casual. Aquest projecte té finalitat exclusivament formativa i demostrativa.

---

## 📄 Llicència

Aquest projecte es distribueix sota llicència **MIT**. Pots utilitzar, modificar i distribuir lliurement el codi per a qualsevol ús, incloent-hi el comercial, sempre que mantinguis l'atribució original.

---

## 🤝 Contribucions

Les contribucions són benvingudes. Si vols afegir nous mòduls d'anàlisi, millorar el prototip o adaptar el checklist a altres normatives (NIIF, US GAAP, etc.), obre un *pull request* o un *issue*.

---

*Generat amb [Claude](https://claude.ai) d'Anthropic · Exercici de tancament 2025*
