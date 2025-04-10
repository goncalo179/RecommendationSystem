<<<<<<< HEAD

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
!git clone https://github.com/goncalo179/LeadPrioritization.git
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

=======
# RecommendationSystem
>>>>>>> cf8580d2e44e2f674aa97eba931dd74d5c0b2975
