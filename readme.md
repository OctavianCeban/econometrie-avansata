Pasi pentru a putea rula notebook.

Optiunea 1 (recomadnat)- uv virtual environment
Este nevoie de python, uv, vs code instalate.

* git clone: git clone https://github.com/OctavianCeban/econometrie-avansata.git

* cd econometrie-avansata 
* uv venv .venv
* Activate with: .venv\Scripts\activate  (sau ce va este sugerat in functie de sistemul de operare)
* uv sync  
* uv run python -m ipykernel install --user --name advanced_econometrics --display-name "uv_advanced_econometrics"


Acum ar trebui, ca dupa un reopen / reload window in vs code sa apara la kernel acest virtual environemtn


Optiunea 2 - Conda
Este nevoie de Anaconda si de VS Code instalate.

Daca abia ai instalat Anaconda si VS Code si vrei sa faci un setup mai usor de folosit poti face si urmatorii pasi:

- Adaugati conda la system environments pentru a putea executa comenzi de conda si din alt tip de terminal (https://stackoverflow.com/questions/44515769/conda-is-not-recognized-as-internal-or-external-command)

- Adaugati conda-forge channel (este un canal unde conda cauta pachete pentru a le instala, daca abia ati instalat Anaconda, e posibil sa nu il aveti):
`conda config --add channels conda-forge`.

Vrem sa cream un virtual environments cu pachetele necesare rularii. Pentru asta, folosim un conda environment, instalam in el pachetele din requirements, apoi ii adaugam lui jupyter notebook un kernel cu acest virtual environment.

Pentru a clona acest repository pe masina voastra trebuie sa aveti git instalat (https://git-scm.com/downloads). 

Apoi mergeti intr-un folder special pentru seminar unde va fi tot ce vom lucra la seminar si executati in terminal (fie in VS Code terminalul de acolo, fie in git bash si sa fiti in acel folder):

`git clone https://github.com/OctavianCeban/econometrie-avansata.git`


Pasi:


1. Creaza un conda environment (intr-un terminal, de preferat anaconda powershell prompt), de prefarat cu python 3.12:

`conda create -n econometrie-avansata python=3.12`


Daca te te intreaba "Proceed y\n" apasa `y` si enter
Pentru a vedea virtual environments avute:

`conda env list`

2. Activeaza virtual environment nou creat:

`conda activate econometrie-avansata`

Ar trebui sa apara in stanga in paranteza (econometrie-avansata). Orice instalare de aplicatie se va face de in acest venv creat. In acest moment, poti instala pachete, iar ele se instaleaza doar in acest virtual environemnts (deci nu se contamineaza base sau alt venv cu ele).

3. Instaleaza pachatele necesare din requirements.txt

Trebuie sa fiti in folderul unde exista requirements txt. 
`conda install --file requirements.txt`

Exista si requiremetents de pip. Daca vreti sa folositi pip in loc de conda (ca poate e mai lent sau apar erori de channels) puteti folosi

`pip install -r requirements_pip.txt`

4. Adauga virtual env creat ca si python kernel 

`python -m ipykernel install --user --name econometrie-avansata --display-name "econometrie-avansata"`

Acum ar trebui sa gasiti kernelul la jupyter notebook



