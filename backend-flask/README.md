# Install python version
```
pyenv install 3.10.9
```
FRONTEND_URL="*" BACKEND_URL="*" docker container run --rm -p 4567:4567 -d backend-flask

docker container run --rm -p 4567:4567 -d backend-flask -e.FRONTEND_URL="*" BACKEND_URL="*"

# Set your python version
```
pyenv global 3.10.9
```

# Create virual environment
```
python -m venv venv
```

# Activate environment
```
source venv/bin/activate
```

# Install Flask
```
pip install flask
```