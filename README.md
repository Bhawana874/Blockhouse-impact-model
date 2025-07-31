# Blockhouse-impact-model

## 📌 Problem Summary

When executing a large market order, slippage occurs due to limited liquidity on the order book. The goal is to:
1. Model the temporary market impact function \( g_t(x) \) from order book data.
2. Allocate a total volume of shares \( S \) across multiple time intervals \( t_1, t_2, ..., t_N \) to minimize total execution cost.

## 📊 What’s Inside

- **Order book simulation** based on the PDF-provided data.
- **Slippage computation** using real order book depth.
- **Quadratic model fitting**:  
  \( g_t(x) = \alpha x + \beta x^2 \)
- **Convex optimization** using `cvxpy` to find optimal trade allocation.
- **Visualization** of both the impact function and allocation strategy.

## 🔧 Technologies Used

- Python 3.8+
- NumPy
- Pandas
- Matplotlib
- CVXPY (for convex optimization)

## 🚀 How to Run

1. Open the notebook on [Google Colab](https://colab.research.google.com/drive/1yg_eTnG3WKs6_EAkbgOv0PrvmFySgok6)  
2. Run each cell sequentially  
3. The notebook will:
   - Plot the slippage function
   - Fit a model to it
   - Compute the optimal trade allocation over time

## 📈 Output Example

- Fitted Model:  
  \( g(x) \approx 0.00005x + 0.00000x^2 \)
- Optimal allocation across 10 time intervals:  
  \[30, 30, ..., 30\] shares per interval
- Visuals:
  - Slippage curve
  - Bar chart of share allocation


