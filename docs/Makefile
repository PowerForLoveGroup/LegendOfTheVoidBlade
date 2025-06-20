# Makefile for MkDocs project
# MkDocs项目自动化部署Makefile, 2025.06.20, Deepseek.

# Variables
VENV = venv
PYTHON = $(VENV)/bin/python
PIP = $(VENV)/bin/pip
MKDOCS = $(VENV)/bin/mkdocs
PORT = 8000

# Default target
.DEFAULT_GOAL := help

# Help target to show all available commands
help:
	@echo "MkDocs Project Management"
	@echo ""
	@echo "Available commands:"
	@echo "  make setup      - Set up the development environment"
	@echo "  make serve      - Serve the documentation locally"
	@echo "  make build      - Build the static site"
	@echo "  make deploy     - Deploy to GitHub Pages"
	@echo "  make clean      - Clean up generated files"
	@echo "  make update     - Update MkDocs and dependencies"
	@echo "  make help       - Show this help message"

# Set up the development environment
setup:
	@echo "Setting up development environment..."
	python3 -m venv $(VENV)
	$(PIP) install --upgrade pip
	$(PIP) install mkdocs
	@echo "Environment setup complete."

# Serve the documentation locally
serve:
	@echo "Starting MkDocs development server..."
	$(MKDOCS) serve -a 0.0.0.0:$(PORT)
	@echo "Server running at http://localhost:$(PORT)."

# Build the static site
build:
	@echo "Building static site..."
	$(MKDOCS) build
	@echo "Site built in 'site/' directory."

# Deploy to GitHub Pages
deploy:
	@echo "Deploying to GitHub Pages..."
	$(MKDOCS) gh-deploy --clean
	@echo "Deployment complete. Check your GitHub Pages site."

# Clean up generated files
clean:
	@echo "Cleaning up..."
	rm -rf site/
	@echo "Clean complete."

cleanvenv:
	@echo "Cleaning up virtual environment..."
	rm -rf $(VENV)
	@echo "Clean complete."

# Update MkDocs and dependencies
update:
	@echo "Updating MkDocs and dependencies..."
	$(PIP) install --upgrade mkdocs mkdocs-material
	@echo "Update complete."

.PHONY: help setup serve build deploy clean update