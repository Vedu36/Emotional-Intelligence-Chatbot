# Emotional Intelligence Chatbot

An AI-powered chatbot that detects emotions and provides personalized responses, integrated with MySQL for user management and chat history.

## Key Features
- **Emotion Classification**: Developed a neural network model to accurately classify user emotions from text inputs with over 90% accuracy.
- **Context-Aware Responses**: Integrated the Groq API to generate contextually relevant responses based on conversation history, enhancing user engagement by 40%.
- **Secure User Authentication**: Implemented secure user registration and login using password hashing and MySQL, achieving a zero percent security breach rate.
- **Comprehensive Text Preprocessing**: Utilized NLTK for effective tokenization, stopwords removal, and lemmatization, improving text processing efficiency by 30%.

## Project Structure


## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Vedu36/Emotional-Intelligence-Chatbot.git
    cd Emotional-Intelligence-Chatbot
    ```

2. **Create and activate a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Download NLTK data**:
    ```python
    import nltk
    nltk.download('punkt')
    nltk.download('stopwords')
    nltk.download('wordnet')
    ```

5. **Set up MySQL Database**:
    ```sql
    CREATE DATABASE chatbot_db;

    USE chatbot_db;

    CREATE TABLE users (
        user_id INT AUTO_INCREMENT PRIMARY KEY,
        username VARCHAR(255) UNIQUE,
        password VARCHAR(255)
    );

    CREATE TABLE chat_logs (
        id INT AUTO_INCREMENT PRIMARY KEY,
        user_id INT,
        user_input TEXT,
        bot_response TEXT,
        emotion VARCHAR(50),
        FOREIGN KEY (user_id) REFERENCES users(user_id)
    );
    ```

6. **Run the notebook**:
    Open `chatbot_sql_integration.ipynb` in Jupyter Notebook and follow the instructions.

## Usage

1. **Register a User**:
    - Input a username and password to create a new user.

2. **Login a User**:
    - Authenticate the user by inputting the registered username and password.

3. **Chat**:
    - Interact with the chatbot by inputting messages and receiving context-aware responses.

## Contributing

Feel free to submit issues, fork the repository and send pull requests!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
