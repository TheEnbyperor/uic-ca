all: build/certificate-policy.html build/certificate-policy.pdf

venv:
	python3 -m venv venv
	venv/bin/pip install xml2rfc[pdf]

build:
	mkdir build

build/certificate-policy.html: certificate-policy.xml venv build
	venv/bin/xml2rfc --html -p build certificate-policy.xml

build/certificate-policy.pdf: certificate-policy.xml venv build
	venv/bin/xml2rfc --pdf -p build certificate-policy.xml