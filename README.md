
# Amazon Electronics Recommendation System

This project builds a recommendation system for Amazon's electronics products using collaborative filtering techniques.
The goal is to improve user experience by suggesting relevant products based on historical rating patterns.

## Project Structure
- **data/**: Contains the raw data files ("ratings_Electronics.csv").
- **notebooks/**: Jupyter notebooks with data cleaning, visualization, and analysis ("Amazon_Product_Recommendation_System.ipynb").
- **requirements.txt**: Dependencies needed to run the project.

## Key Insights
- Preprocessing of user-product ratings data
- Building recommendation system using ranking, similarity-based methods, SVD
- Baseline model comparisons using recall, precision, RMSE, and F1
- Hyperparameter tuning of the different models using GridSearchCV
- Final model selection based on evaluation metrics

## Requirements
- Google Colab (Recommended) - Python 3.x pre-installed
- OR Local Setup - Requires Python 3.x (Download from python.org)
- Install required packages from "requirements.txt"

**Note:** If you're using Google Colab, prefix commands with "!", e.g., "!git clone ...". On a local setup, use the commands without "!", e.g., "git clone ...".


## Usage
1. Clone the repository:

```bash
!git clone https://github.com/goncalo179/RecommendationSystem.git
```

2. Install dependencies:

```bash
!pip install -r requirements.txt
```

3. Open and run the Jupyter Notebook.

**Note:** scikit-surprise is not yet compatible with numpy>=2.0.
Make sure to install numpy<2.0 (this is already handled in requirements.txt, but worth noting here in case of manual installations)

## Troubleshooting

**ImportError: numpy.core.multiarray failed to import**
This usually happens if you're using "numpy>=2.0", which is incompatible with "scikit-surprise". To fix it, run:

```bash
!pip install "numpy<2.0"
```


## Dataset
This project uses the [Amazon Product Reviews dataset](https://www.kaggle.com/datasets/goncalo179/amazon-electronics-ratings) available on Kaggle.

## Option 1: Manual Download (Quick & Easy)
You can download the CSV file directly by visiting the Kaggle page linked above.
After downloading, unzip the file and place ratings_Electronics.csv in the data/ folder of this project.

## Option 2: Use Kaggle API (for reproducible notebooks and automation)
If you prefer downloading via code (especially useful when working in Google Colab), follow the instructions below to set up the Kaggle API.


## Setting Up Kaggle API Access

1. Create a Kaggle account if you don't have one already: [Kaggle Sign-Up](https://www.kaggle.com).
2. Navigate to your Kaggle account settings page [here](https://www.kaggle.com/settings) and click "Create New API Token". This will download a `kaggle.json` file containing your API credentials.
3. Upload the "kaggle.json" file to your Colab environment or store it securely in your local setup.


## Upload kaggle.json manually (recommended for one-time use)

- Go to your Kaggle account → Account → Create New API Token
- This downloads a file called kaggle.json.
- Upload it to Colab using the code below:

```bash
from google.colab import files
files.upload()  # Upload kaggle.json manually

!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
```

### Load from Google Drive (if stored there securely)

- If you prefer storing your kaggle.json in Google Drive (e.g. inside a private folder)

```bash
from google.colab import drive
drive.mount("/content/drive")

!mkdir -p ~/.kaggle
!cp /content/drive/MyDrive/<folder_name>/kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
```

# Download the dataset

```bash
!kaggle datasets download -d goncalo179/amazon-electronics-ratings
```

# Unzip the dataset

```bash
# Make a data/ directory if it doesn't exist
!mkdir -p data/

# Unzip the dataset into the data/ folder
!unzip -q amazon-electronics-ratings.zip -d data/
```
