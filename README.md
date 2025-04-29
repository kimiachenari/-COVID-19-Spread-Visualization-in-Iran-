# 📉 **COVID-19 Spread Visualization in Iran** 🇮🇷

This project visualizes the spread of **COVID-19** in various regions of **Iran** over several weeks. The data includes reported case numbers for specific dates, and the visualization uses **scatter plots** to show the increase in cases across different regions. The size of each scatter point is proportional to the number of cases, and the colors represent different time periods in the spread.

---

## 🚀 **Key Features**

- **Scatter Plot Visualization**: Shows the spread of COVID-19 cases over time for different regions of Iran.
- **Color Gradient**: Each point is color-coded by the date of the report, providing a clear visual of the disease's progression.
- **Size Proportionality**: The size of each point reflects the number of reported cases for that region, making it easy to compare the magnitude of the spread.
- **Data Import**: The data is imported from a **CSV file** containing case numbers for specific dates.

---

## 🧑‍🔬 **Getting Started**

### 1. **Install Required Libraries**

Ensure that you have the necessary libraries installed:

```bash
pip install pandas matplotlib
```

### 2. **Prepare the Data**

Make sure your **CSV file** (e.g., `datafinal1.csv`) contains the necessary columns, including:

- `region`: The regions of Iran.
- `number98/12/07`, `number98/12/13`, `number98/12/19`, `number98/12/25`, `number99/01/02`: The reported COVID-19 cases for different dates.

### 3. **Run the Script**

1. **Set the File Path**: Update the file path for your **CSV** file.
2. **Execute the Script**: Run the script to generate a scatter plot visualization of the COVID-19 spread in Iran.

---

## 🔧 **How It Works**

### 1. **Import Libraries**

The script imports the required libraries: **Matplotlib** for plotting, and **Pandas** for handling the CSV data.

```python
from matplotlib.pyplot import figure
import matplotlib.pyplot as plt
import pandas as pd
```

### 2. **Read Data**

The data is read from the **CSV file** using **Pandas**, which is then converted into a **DataFrame** for further processing:

```python
file2 = 'C:/Users/kimia/Desktop/New folder (2)/datafinal1.csv'
dataf = pd.read_csv(file2)
df = pd.DataFrame(dataf)
```

### 3. **Prepare the Data**

The script extracts the **regions** and **reported cases** for each date:

```python
x = dataf["region"]
y1 = dataf["number98/12/07"]
y2 = dataf["number98/12/13"]
y3 = dataf["number98/12/19"]
y4 = dataf["number98/12/25"]
y5 = dataf["number99/01/02"]
```

### 4. **Set Area Size Proportions**

The size of each point on the scatter plot is proportional to the number of cases for each region:

```python
area1 = (0.1 * y1)
area2 = (0.2 * y2)
area3 = (0.3 * y3)
area4 = (0.4 * y4)
area5 = (0.5 * y5)
```

### 5. **Create Scatter Plot**

The script generates a scatter plot with points color-coded by the date and sized according to the number of reported cases:

```python
plt.scatter(y1, x, s=area1, color="#fa0000", alpha=0.5)
plt.scatter(y2, x, s=area2, color="#d10000", alpha=0.5)
plt.scatter(y3, x, s=area3, color="#9e0000", alpha=0.5)
plt.scatter(y4, x, s=area4, color="#850000", alpha=0.5)
plt.scatter(y5, x, s=area5, color="#140000", alpha=0.5)
```

### 6. **Adjust Plot Size and Save**

The plot size is adjusted to ensure clarity, and the final plot is saved as a high-resolution **JPEG** image:

```python
fig = plt.figure()
plt.rcParams.update({'font.size':4})

output_dir = "C:/Users/kimia/Desktop/New folder (2)"
fig.savefig('{}/graph5.jpg'.format(output_dir), dpi = 500)
```

---

## 📊 **Outputs**

- **Scatter Plot**: A visualization showing the spread of COVID-19 in different regions of Iran. The points represent regions, with size proportional to the number of reported cases, and color-coded by the report date.
- **Saved Image**: The final plot is saved as a **JPEG** image with high resolution for further use.

---

## 📈 **Future Enhancements**

- **Interactivity**: Integrate interactive visualization tools like **Plotly** or **Bokeh** to allow users to explore the data interactively.
- **Time Series**: Create an animated visualization that shows the changes in COVID-19 cases over time.
- **Comparison**: Add the ability to compare different regions or countries based on the spread of COVID-19.

---
![final_gragh](https://github.com/user-attachments/assets/ed9a69df-7bbf-409d-bd63-3d396ce8588c)

![final_graph4](https://github.com/user-attachments/assets/c60338d8-08be-4fef-a030-76ade2589b5c)

