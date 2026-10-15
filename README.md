# Telecom Customer Churn Analysis (PwC case study)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dukehoangwrk/telecom-churn-analysis/blob/main/telecom_churn_analysis.ipynb)

Phân tích khách hàng rời mạng của một công ty viễn thông (3.333 khách, 21 cột) theo brief của PwC: ai đang rời đi, yếu tố nào ảnh hưởng nhiều nhất, và làm sao dự đoán sớm.

## Kết quả chính
- Tỷ lệ churn **14,5%**, nhóm này chiếm 15,9% tổng cước.
- Ba dấu hiệu rủi ro: gọi tổng đài từ 4 lần (churn 52%), hóa đơn trên 70$ (43%), có gói quốc tế (42%). Ba nhóm này chỉ chiếm 29% khách nhưng chứa **88%** số khách rời đi.
- Gói quốc tế không giảm giá phút gọi (vẫn 0,27$/phút); toàn bộ 111 khách dùng gói không phù hợp đều đã rời đi.
- XGBoost: recall 80%, precision 100%, AUC 0,92. Liên hệ 15% khách rủi ro cao nhất bắt được 84% khách sắp rời đi.

## Nội dung
| File | Mô tả |
|---|---|
| `telecom_churn_analysis.ipynb` | Notebook phân tích (EDA, kiểm định, mô hình) |
| `report/Telecom_Churn_Report.pdf` | Báo cáo 10 trang |
| `data/telco_churn.csv` | Dữ liệu |
| `figures/` | Biểu đồ |

## Cách chạy
- Máy cá nhân: `pip install -r requirements.txt` rồi mở notebook.
- Google Colab: bấm badge ở trên, Runtime → Run all, chọn file `data/telco_churn.csv` khi được hỏi.

Công cụ: Python (pandas, seaborn, scipy, scikit-learn, XGBoost).
