Pasi pentru a putea rula notebook.
Este nevoie de Anaconda instalat. 

1. Creaza un conda environment (intr-un terminal):

`conda create -n econometrie-avansata`


Daca te te intreaba "Proceed y\n" apasa `y` si enter

2. Pentru a vedea virtual environments avute:

`conda env list`

3. Activeaza virtual environment nou creat:

`conda activate econometrie-avansata`

Ar trebui sa apara in stanga in paranteza (econometrie-avansata). Orice instalare de aplicatie se va face de in acest venv creat. 

4. Instaleaza pachatele necesare din requirements.txt

conda install --file requirements.txt

5. Adauga virtual env creat ca si python kernel 

`python -m ipykernel install --user --name econometrie-avansata --display-name "econometrie-avansata"`

Acum ar trebui sa gasiti kernelul la jupyter notebook





