.PHONY: install clean run setup

VENV := .venv
PYTHON := $(VENV)/bin/python3
JUPYTER := $(VENV)/bin/jupyter

# Setup virtual environment
setup:
	python3 -m venv $(VENV)
	$(PYTHON) -m pip install --upgrade pip

# Install the project dependencies
install: setup
	$(PYTHON) -m pip install -r requirements.txt

# Clean up the project directory
clean:
	rm -rf $(VENV)
	rm -rf __pycache__/
	rm -rf .pytest_cache/
	rm -rf build/
	rm -rf dist/
	rm -rf *.egg-info
	find . -type f -name '*.pyc' -delete
	find . -type d -name '__pycache__' -delete

# Run the application
run: install
	$(JUPYTER) notebook
