# solving_captchas_using_deep_learning

In this repository we use deep learning to crack the captchas.

There are four Jupyter Notebook and one zip file of dataset.
dataset - generated_captcha_images.zip

These files can be run using docker. Docker can be downloaded from
- https://www.docker.com/get-docker

Then open a terminal and type - 
```shell
docker run -itd \
  --restart always \
  --name captchas \
  -p 8888:8888 \
  jupyter/tensorflow-notebook \
  start-notebook.sh --NotebookApp.token=''
```
Docker will start after running this command.
Now go to the browser and open URL : http://localhost:8888
Jupyter notebook will run.

## Setting up Notebooks
Download the notebooks from this repository and load it into your Jupyter notebook workspace.
Make a folder "dataset/" and load your data in that folder.

## Run
- First run "Unzip data.ipynb". This will unzip the data.
- Next run "extract_single_letters_from_captchas.ipynb". This creates new data in dataset/extracted_letter_images folder.
- Now run "train_model.ipynb" for training.
- Lastly, run "solve_captchas_with_model.ipynb" for solving some random captcha images.

