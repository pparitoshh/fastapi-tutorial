# FastAPI Tutorial

This repository contains a learning project for FastAPI, a modern, fast web framework for building APIs with Python.

## Project Structure
```
fastapi-tutorial/
├── main.py              # Main FastAPI application
├── notes/              # Learning notes and documentation
│   └── first_steps.md  # First steps with FastAPI
├── requirements.txt    # Project dependencies
└── README.md          # This file
```

## Setup Instructions

### 1. Create Conda Environment
```bash
# Create a new conda environment with Python 3.11
conda create -n fastapi python=3.11 -y

# Activate the environment
conda activate fastapi
```

### 2. Install Dependencies
```bash
# Install all required packages
pip install -r requirements.txt
```

### 3. Run the Application
```bash
# Start the development server
fastapi dev main.py
```

The server will start at http://127.0.0.1:8000

## API Documentation
- Interactive API docs (Swagger UI): http://127.0.0.1:8000/docs
- Alternative API docs (ReDoc): http://127.0.0.1:8000/redoc

## Learning Resources
- [FastAPI Official Documentation](https://fastapi.tiangolo.com/)
- [FastAPI GitHub Repository](https://github.com/tiangolo/fastapi)

## Notes
- Check the `notes/` directory for detailed learning notes
- The project follows FastAPI best practices and conventions
- All code examples are documented with comments

## Contributing
Feel free to contribute to this learning project by:
1. Forking the repository
2. Creating a new branch
3. Making your changes
4. Submitting a pull request

## License
This project is open source and available under the MIT License. 