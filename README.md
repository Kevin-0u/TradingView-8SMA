# SMA Cloud, Multi-SMA & Parabolic SAR Indicator

A **TradingView Pine Script indicator** that combines:

- Up to **eight customizable Simple Moving Averages (SMAs)**
- A dynamic **SMA Cloud** between the first two SMAs
- The classic **Parabolic SAR** trend-following indicator

It’s designed to help you quickly spot trend direction, support/resistance, and momentum shifts — all in one clean view.

## 🚀 Key Features (For Traders)

- **SMA Cloud**
  A shaded cloud is drawn between the first two SMAs, helping you visualize when price is trending vs consolidating.
  > ℹ️ If either of the first two SMAs is hidden, the cloud won’t appear.

- **Multiple SMAs**
  Track up to 8 SMAs at once. Configure each length independently to fit your style — from short-term momentum (5–10 bars) to long-term trends (100–200 bars).

- **Parabolic SAR**
  Built-in SAR points appear above or below price, highlighting potential trend reversals and trailing stop levels.

- **Toggle Visibility**
  Show or hide each SMA and the SAR indicator individually, both on the chart and in the summary table, keeping your workspace clean.

- **Color-Coded Summary Table**
  A compact table at the top of the chart displays the latest SMA values (and optionally SAR), color-coded for quick interpretation.

## 📈 Why Use This Indicator?

- Confirm trend direction with SMAs and SMA Cloud.
- Identify momentum shifts when SMAs cross or SAR flips position.
- Use SAR as a trailing stop guide to lock in profits.
- Keep charts uncluttered with a consolidated SMA/SAR overview table.

## ⚙️ How to Use

1. Add the indicator to your TradingView chart.
2. Open the settings panel to configure:
   - Up to 8 SMA lengths
   - SAR parameters (step, maximum)
3. Choose which SMAs and whether SAR should be shown on chart and/or in the summary table.
4. Use the SMA Cloud and SAR together for trend confirmation and potential entry/exit signals.

---

## 🛠 Developer Notes

This section is for developers who want to extend, debug, or adapt the script.

### Core Components

- **SMA Cloud**
  A filled region between SMA1 and SMA2. The cloud is only drawn if both are enabled.

- **SMA Management**
  - Each SMA has an independent length input.
  - Visibility can be toggled for chart plotting and table display.

- **Parabolic SAR**
  - Standard TradingView `sar()` function implementation.
  - Configurable step and maximum parameters.
  - Plotted as dots above/below price; optional inclusion in summary table.

- **Summary Table**
  - Displays the most recent values of all enabled SMAs.
  - SAR value can be displayed if enabled.
  - Colors match chart plots for consistency.

### Implementation Notes

- Table rendering is dynamic: disabled SMAs and SAR are excluded.
- SMA Cloud rendering depends on SMA1 and SMA2 being visible; otherwise, no fill is drawn.
- SAR updates per bar, flipping when trend direction changes.
