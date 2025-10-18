# Contributing to Telco Customer Churn Prediction

First off, thank you for considering contributing to this project! 🎉

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Pull Request Process](#pull-request-process)
- [Style Guidelines](#style-guidelines)
- [Community](#community)

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code. Please be respectful and constructive in all interactions.

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include:

- **Clear title and description**
- **Steps to reproduce** the issue
- **Expected vs actual behavior**
- **Screenshots** if applicable
- **Environment details** (OS, Python version, library versions)

### 💡 Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Clear title and description**
- **Use case** for the enhancement
- **Expected benefits**
- **Possible implementation approach** (optional)

### 📝 Code Contributions

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Make your changes**
4. **Write/update tests** if applicable
5. **Update documentation** as needed
6. **Commit with clear messages** (`git commit -m 'Add some AmazingFeature'`)
7. **Push to your branch** (`git push origin feature/AmazingFeature`)
8. **Open a Pull Request**

## Getting Started

### Prerequisites

- Python 3.8+
- Git
- Virtual environment tool (venv, conda, etc.)

### Setup Development Environment

```bash
# Clone your fork
git clone https://github.com/shreyashpatil530/Telco-Customer-Churn-Prediction.git
cd Telco-Customer-Churn-Prediction

# Add upstream remote
git remote add upstream https://github.com/ShreyashPatil530/Telco-Customer-Churn-Prediction.git

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install development dependencies
pip install pytest black flake8 pylint
```

## Pull Request Process

1. **Update documentation** for any new features
2. **Update the README.md** if needed
3. **Add tests** for new functionality
4. **Ensure all tests pass**
5. **Follow code style guidelines**
6. **Write clear commit messages**
7. **Link related issues** in PR description
8. **Request review** from maintainers

### PR Title Format

```
<type>: <description>

Types:
- feat: New feature
- fix: Bug fix
- docs: Documentation changes
- style: Code style changes (formatting)
- refactor: Code refactoring
- test: Adding or updating tests
- chore: Maintenance tasks

Examples:
- feat: Add LSTM model for churn prediction
- fix: Handle missing values in TotalCharges column
- docs: Update installation instructions
```

## Style Guidelines

### Python Code Style

- Follow **PEP 8** guidelines
- Use **4 spaces** for indentation
- Maximum line length: **100 characters**
- Use **type hints** where applicable
- Write **docstrings** for functions and classes

### Code Formatting

```bash
# Format code with Black
black src/

# Check code style
flake8 src/

# Run linter
pylint src/
```

### Example Function

```python
def predict_churn(customer_data: pd.DataFrame) -> np.ndarray:
    """
    Predict customer churn probability.
    
    Args:
        customer_data: DataFrame containing customer features
        
    Returns:
        Array of churn probabilities
        
    Raises:
        ValueError: If required columns are missing
    """
    # Implementation here
    pass
```

### Commit Message Guidelines

- Use present tense ("Add feature" not "Added feature")
- Use imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit first line to 72 characters
- Reference issues and PRs in description

```
Good: Add feature to handle missing values
Bad: added feature for handling missing values
```

### Documentation

- Update README.md for user-facing changes
- Add inline comments for complex logic
- Update docstrings when modifying functions
- Include examples in docstrings

## Testing

### Running Tests

```bash
# Run all tests
pytest

# Run specific test file
pytest tests/test_preprocessing.py

# Run with coverage
pytest --cov=src tests/
```

### Writing Tests

```python
import pytest
from src.preprocessing import handle_missing_values

def test_handle_missing_values():
    """Test missing value handling."""
    # Arrange
    data = pd.DataFrame({'col': [1, None, 3]})
    
    # Act
    result = handle_missing_values(data)
    
    # Assert
    assert result['col'].isnull().sum() == 0
```

## Project Structure

When adding new files, follow this structure:

```
src/
├── data/
│   ├── preprocessing.py
│   └── feature_engineering.py
├── models/
│   ├── train.py
│   └── predict.py
├── utils/
│   └── helpers.py
└── visualization/
    └── plots.py
```

## Areas for Contribution

### Priority Areas

- [ ] Implement deep learning models
- [ ] Add real-time prediction API
- [ ] Create interactive dashboard
- [ ] Improve model interpretability
- [ ] Add automated testing pipeline

### Good First Issues

Look for issues labeled `good first issue` or `help wanted` for beginner-friendly contributions.

## Recognition

Contributors will be:
- Listed in README.md
- Mentioned in release notes
- Added to CONTRIBUTORS.md file

## Questions?

Feel free to:
- Open an issue for questions
- Reach out via email: shreyashpatil530@gmail.com
- Connect on LinkedIn

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing! 🚀**

*Happy Coding!*
