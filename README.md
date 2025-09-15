# SMA Cloud & Multi-SMA Indicator

A **TradingView Pine Script indicator** that lets you track up to **eight customizable Simple Moving Averages (SMAs)** in one clean view.  
It’s designed to make trend direction, support/resistance zones, and momentum shifts easier to see at a glance.

---

## 🚀 Key Features (For Traders)

- **SMA Cloud**  
  A shaded cloud is drawn between the first two SMAs, helping you visualize when price is trending vs consolidating.  
  > ℹ️ If either of the first two SMAs is hidden, the cloud won’t appear.

- **Flexible Setup**  
  Define the length of each SMA to fit your trading style — from short-term momentum (5–10 bars) to long-term trend following (100–200 bars).

- **Toggle Visibility**  
  Show or hide each SMA individually, both on the chart and in the summary table, keeping your workspace clean.

- **Color-Coded Summary Table**  
  A compact table at the top of the chart displays the latest SMA values, color-coded for quick interpretation.

---

## 📈 Why Use This Indicator?

- Confirm trend direction at a glance with multiple SMAs.  
- Identify bullish/bearish momentum shifts when SMAs cross and the SMA cloud changes color.  
- Keep charts uncluttered with a streamlined SMA overview table.  

---

## ⚙️ How to Use

1. Add the indicator to your TradingView chart.  
2. Open the settings panel to configure up to 8 SMA lengths.  
3. Decide which SMAs to display on the chart and in the summary table.  
4. Use the SMA Cloud (first two SMAs) as a visual cue for trend strength and possible reversals.  

---

## 🛠 Developer Notes

This section is for developers who want to extend, debug, or adapt the script.

### Core Components

- **SMA Cloud**  
  A filled region between SMA1 and SMA2. The cloud is only drawn if both are enabled.  

- **SMA Length Customization**  
  Each SMA has its own configurable length input. Default values can be adjusted for short-, mid-, or long-term analysis.  

- **Visibility Controls**  
  Each SMA can be individually toggled for:  
  - **Chart plotting** (line visibility)  
  - **Table display** (inclusion/exclusion from summary table)  

- **Summary Table**  
  Displays the most recent value of each enabled SMA at the top of the chart. Colors match the plotted SMA lines.  

### Implementation Notes

- Table rendering is dynamic: disabled SMAs are excluded.  
- SMA Cloud rendering depends on SMA1 and SMA2 being visible; otherwise, no fill is drawn.  

---
