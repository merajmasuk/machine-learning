PROJECT="MyML"
AUTHOR="Meraj al Maksud"
RELEASE="0.0.0.1"


install:
	pip install -r requirements.txt

docs:
	echo "Generating docs..." && \
	cd docs && \
	sphinx-quickstart -q -p $(PROJECT) -a $(AUTHOR) -r $(RELEASE) --ext-viewcode --ext-todo --ext-autodoc && \
	cd .. && \
	cd my_py_pkg && \
	sphinx-apidoc -o ../docs src/

build:
	python3 setup.py sdist bdist_wheel

publish: build
	twine upload dist/*

.PHONY: docs
