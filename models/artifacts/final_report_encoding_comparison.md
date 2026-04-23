# Отчёт по сравнению моделей и методов кодирования

        ## Базовые модели (параметры по умолчанию)
        | encoding   | model                   |   roc_auc |   pr_auc |       f1 |
|:-----------|:------------------------|----------:|---------:|---------:|
| onehot     | onehot_GradientBoosting |  0.954692 | 0.164029 | 0.307406 |
| onehot     | onehot_XGBoost          |  0.95426  | 0.162333 | 0.307642 |
| onehot     | onehot_CatBoost         |  0.954862 | 0.164126 | 0.307715 |
| onehot     | onehot_LightGBM         |  0.954487 | 0.164802 | 0.307597 |
| label      | label_GradientBoosting  |  0.954867 | 0.164587 | 0.307293 |
| label      | label_XGBoost           |  0.955037 | 0.166176 | 0.307626 |
| label      | label_CatBoost          |  0.95496  | 0.164313 | 0.307638 |
| label      | label_LightGBM          |  0.954842 | 0.167316 | 0.30769  |
| target     | target_GradientBoosting |  0.954842 | 0.164867 | 0.30714  |
| target     | target_XGBoost          |  0.954431 | 0.164784 | 0.307603 |
| target     | target_CatBoost         |  0.955079 | 0.164693 | 0.307692 |
| target     | target_LightGBM         |  0.954535 | 0.164159 | 0.307571 |

        ## Настроенные модели (после GridSearchCV)
        | encoding   | model                         |   roc_auc |   pr_auc |       f1 |
|:-----------|:------------------------------|----------:|---------:|---------:|
| onehot     | onehot_GradientBoosting_tuned |  0.954508 | 0.163555 | 0.30767  |
| onehot     | onehot_XGB_tuned              |  0.954875 | 0.163211 | 0.307545 |
| onehot     | onehot_LGBM_tuned             |  0.95465  | 0.163288 | 0.306713 |
| onehot     | onehot_CATBoost_tuned         |  0.955358 | 0.166379 | 0.307741 |
| label      | label_GradientBoosting_tuned  |  0.954098 | 0.163195 | 0.307715 |
| label      | label_XGB_tuned               |  0.955294 | 0.165737 | 0.307749 |
| label      | label_LGBM_tuned              |  0.95533  | 0.165926 | 0.307632 |
| label      | label_CATBoost_tuned          |  0.955586 | 0.168782 | 0.307727 |
| target     | target_GradientBoosting_tuned |  0.954519 | 0.163287 | 0.307678 |
| target     | target_XGB_tuned              |  0.955266 | 0.164371 | 0.30765  |
| target     | target_LGBM_tuned             |  0.954457 | 0.163763 | 0.306673 |
| target     | target_CATBoost_tuned         |  0.955225 | 0.166672 | 0.307751 |

        ## Лучшие результаты
        - **Базовые модели:**
        - ROC-AUC: target_CatBoost (0.9551)
        - PR-AUC: label_LightGBM (0.1673)
        - **Настроенные модели:**
        - ROC-AUC: label_CATBoost_tuned (0.9556)
        - PR-AUC: label_CATBoost_tuned (0.1688)

        Все эксперименты сохранены в MLflow (`../mlruns`).
        