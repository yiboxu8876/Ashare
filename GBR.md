```
py -3.12 acquire.py
```
```
py -3.12 GBR-CV.py
```
```
py -3.12 make_predict_dirs.py
```
```
for /L %i in (0,1,19) do (del /q "%i\data.xlsx" "%i\predict.py" "%i\HP-Screening.xlsx" "%i\predictions.csv" "%i\predictions.xlsx" 2>nul & copy /y "data.xlsx" "%i\" & copy /y "predict.py" "%i\" & copy /y "HP-Screening.xlsx" "%i\")
```
```
py -3.12 update_predict_change.py
```
```
for /d %d in (*) do (
    cd "%d"
    py -3.12 predict.py
    cd ..
)
```
```
py -3.12 collect_predictions.py
```
