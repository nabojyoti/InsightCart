# 🛍️ InsightCart: Flask-Based Web Application for Product Recommendation  

**InsightCart** is a machine learning-powered **Flask-based web application** for product recommendation, designed to deliver personalized suggestions. Built with the **Singular Value Decomposition (SVD)** algorithm, this system leverages collaborative filtering to provide accurate and tailored recommendations. The application is fully containerized using Docker, making deployment seamless and efficient.  

---

## 🚀 Features  

- **Flask Web Application**: A responsive web interface where users can select user IDs and product IDs to get personalized product recommendations.  
- **Machine Learning Model**: The recommendation model is trained using the `scikit-surprise` library with SVD for collaborative filtering.  
- **Dockerized Application**: The app is fully containerized with Docker, ensuring easy portability and consistent environment setup.  
- **Interactive Web Interface**: Styled using Bootstrap, the interface is clean and user-friendly.  
- **Modular Project Structure**: Separates logic for model loading, web interface, and prediction for better scalability and maintainability.  

---

## 💻 Tech Stack  

- **Programming Language**: Python
- **Web Framework**: Flask  
- **Machine Learning**: scikit-surprise (SVD algorithm)  
- **Frontend Styling**: Bootstrap  
- **Containerization**: Docker, Docker Compose  

---

## 🗂️ Project Structure  

```
InsightCart/
├── app.py                 # Main Flask application
├── Dockerfile             # Dockerfile to containerize the Flask app
├── docker-compose.yml     # Docker Compose for managing the Docker container
├── requirements.txt       # Python dependencies for the project
├── model/
│   └── svd_model.pkl      # Trained SVD model
└── templates/
    ├── index.html         # HTML template for the form (input)
    └── result.html        # HTML template for displaying recommendation results
```

## 🛠️ Getting Started

### Prerequisites

- **Docker**: You need Docker installed to run the application.
- **Docker Compose**: Ensure Docker Compose is installed for easy container management.

### Running the Application

1. Clone the repository:

    ```bash
    git clone https://github.com/nabojyoti/InsightCart.git
    cd InsightCart
    ```

2. Build and run the Docker container using Docker Compose:

    ```bash
    docker-compose up --build
    ```

3. Open your browser and go to `http://localhost:5000`.

4. Select a user ID and product ID from the dropdowns to get a product recommendation based on the trained model.

### Stopping the Application

To stop the running application, you can use:

```bash
docker-compose down
```

## 🧰 Customization

- **Model Update**: Retrain and replace the `svd_model.pkl` file in the `model/` directory using your data and the scikit-surprise library.

- **Data Integration**: Add support for real-time data by integrating a database such as `PostgreSQL`.

## 🔮 Future Enhancements

- **Database Integration**: Store user and product data in a relational database (e.g., PostgreSQL 🐘).
- **CI/CD Pipelines**: Automate testing and deployment with `GitHub Actions` or `Jenkins`.
- **Cloud Deployment**: Deploy on AWS, GCP, or Azure for global accessibility.
- **Enhanced UX/UI**: Improve frontend design with Bootstrap or Materialize CSS.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
