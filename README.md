#  Sydney Airbnb Price Prediction

An end-to-end Machine Learning regression project designed to estimate fair nightly rental prices for Airbnb listings across Sydney, Australia. The project spans raw data ingestion, robust exploratory analysis, geospatial feature engineering, leak-free preprocessing, hyperparameter optimization, and real-world listing evaluation.

##   Project Overview

Pricing short-term rentals appropriately is crucial for hosts to optimize revenue and occupancy rates, as well as for guests looking for fair pricing. This project builds and compares multiple supervised learning models to predict listing prices based on structural characteristics, host reputation, property types, and geospatial coordinates relative to central Sydney.

###  Key Highlights
- **Geospatial Feature Engineering:** Computed exact geodesic distances to the Sydney Central Business District (CBD) using the **Haversine formula**.
- **Leak-Free Data Pipeline:** Strict separation between training and test sets before any median imputation, rare category encoding, or scaling.
- **Model Diversity & Regularization:** Evaluated Ordinary Least Squares (OLS), Ridge (L2), Lasso (L1), Elastic Net, Decision Trees, and Random Forests.
- **Automated Hyperparameter Tuning:** Systematic search across parameter grids via `GridSearchCV` with 5-fold cross-validation.
- **Feature Explainability:** Extracted feature importances to highlight the key price drivers in the Sydney market.
- **Practical Application:** Simulated inference for an actual high-end property in Bondi Beach.

##  Dataset Description

The project utilizes the public Sydney Airbnb dataset containing over 27,000 listing records with comprehensive features:
- **Location:** Latitude, longitude, neighbourhood cleansed.
- **Capacity & Layout:** Accommodates, bedrooms, beds, bathrooms, room type, property type.
- **Pricing & Policies:** Nightly price, cleaning fees, security deposit, minimum nights.
- **Reviews & Host Metrics:** Review score ratings, reviews per month, superhost status, response rate, identity verification.

##  Practical Application: Bondi Beach Case Study
To validate the model in a realistic business scenario, an unseen sample property in **Bondi Beach** was passed through the pipeline:
- **Features:** 5 Bedrooms, 3 Bathrooms, Accommodates 10, Superhost, Rating 95/100, 255 days availability.
- **Host Listing Price:** `$500.00 / night`
- **Model Valuation (Random Forest):** Predicts a competitive, fair market value based on similar high-demand coastal listings.
