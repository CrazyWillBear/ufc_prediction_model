# UFC Outcome Prediction Model

### Summary
This project uses `scikit-learn`'s Multi-Layer Perceptron (MLP) classifier to make a neural network model that predicts UFC fight outcomes trained on historical fight data. The train/test split was 70/30, I used `LabelEncoder` and `OneHotEncoder` to encode categorical data, and used `StandardScaler` to scale my data. The model, encoders, and scaler are dumped as `.pkl` files using `joblib` for future use in, say, an API. The model itself was tested at ~57% accuracy, which given the unpredictability and frequent upsets within the UFC I'm happy with.

### Data Source
This data comes from Kaggle, [here's the link](https://www.kaggle.com/datasets/mdabbert/ultimate-ufc-dataset).

### Using the Model
- Install required dependencies via `pip install -r requirements.txt`
- You can load the model, scalers, and encoders using the `joblib.load()` function in your own project.

### Project Structure
- `data/` -> dataset csv files
    - `ufc-master.csv` -> historical fight data
    - `upcoming.csv` -> upcoming fight data
- `outputs/` -> html and pdf notebook renders
    - `UFC_Predictor.html`
    - `UFC_Predictor.pdf`
- `pkl_dumps/` -> file dumps of scalers, encoders, and the model itself
    - `scaler.pkl`
    - `ufc_fight_predictor.pkl` -> model dump
    - `X_encoder.pkl`
    - `y_encoder.pkl`
- `UFC_Predictor.ipynb` -> Jupyter notebook file

### License
I use the MIT License, do whatever you want.
