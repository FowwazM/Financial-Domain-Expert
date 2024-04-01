<a name="readme-top"></a>


<!-- PROJECT SHIELDS -->
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/FowwazM/repo_name">
    <img src="Docs/logo.png" alt="Logo" width="100" height="100">
  </a>

<h3 align="center">Financial Domain Expert</h3>

  <p align="center">
    A financial domain expert built with Meta Llama 2
    <br />
    <a href="https://github.com/FowwazM/repo_name"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/FowwazM/repo_name/issues">Report Bug</a>
    ·
    <a href="https://github.com/FowwazM/repo_name/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This is a financial domain expert built by fine-tuning Meta's Llama 2 7B text generation large language model. The model was trained on a financial dataset provided by Amazon (a copy of which can be found in <a href="https://github.com/FowwazM/repo_name/blob/main/financialDataset.txt">this repository</a>) using AWS Sagemaker. The fine-tuned model is able to provide specific facts & statistics relevant to the input prompt and is able to make inferences on the contextual meaning and significance of these facts & statistics to answer prompts.

This project was completed as part of the "Introducing Generative AI" course from AWS. A copy of my certificate of completion of the course is in the `Docs` folder of this repository.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![Sagemaker][Sagemaker-Badge]][Sagemaker-url]
* [![NumPy][Numpy-Badge]][Numpy-url]
* [![Pandas][Pandas-Badge]][Pandas-url]
* [![HuggingFace][Huggingface-Badge]][Huggingface-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get your own copy up and running follow these steps.

### Prerequisites

You will need an AWS account to copy this project. Once you have an account, you need to configure an IAM role and request a GPU instance for training.
* Configuring an IAM role
  * In Amazon Sagemaker, go to the `Role Manager` tab under `Admin configurations` and click "Create a role".
  * Set the role's persona to the "SageMaker Compute Role" option.
  * Under `Configure ML activities`, give the role the permissions shown in the photo below.
  [PHOTO]
  * Under `Add additional IAM policies to this role`, select the "AmazonSageMakerFullAccess" option.
* Request a GPU instance for training
  * Open the AWS Service Quota Dashboard and choose "Sagemaker" in the `AWS Services` dropdown.
  * Under `Service quotas` search for a `ml.g5.2xlarge` instance.
  * Locate the row that says `ml.g5.2xlarge for training job` usage, and fill in the circle next to it.
  * Click on the "Request increase at account-level" button at the top of the page, and enter 1 instances in the request form.

### Installation

1. Create an AWS Sagemaker notebook instance
* In the Sagemaker home page, find the `Notebook` section in the left navigation menu and click the `Notebook instances` tab.
* Click on "Create notebook instance" from the top of the page
* Name your notebook instance and ensure you choose the IAM Sagemaker role you created earlier.
2. Copy the project files
* Download the two Python notebook files (.ipynb) under the `Code` folder in this repository.
* Start your SageMaker notebook instance by clicking on `Open JupyterLab` once the notebook is ready.
* Upload the two Python notebook files to JupyterLab

### Model Deployment

* Open the `Llama2_Model_Evaluation.ipynb` file in JupyterLab and follow the steps in the notebook to deploy the Llama 2 7B LLM from Meta.
* Open the `Model_FineTuning.ipynb` file in JupyterLab and follow the steps in the notebook to fine-tune the LLM and deploy and test your domain expert.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Fowwaz Moeen - [LinkedIn][linkedin-url] - fowwazmoeen@gmail.com

Project Link: [https://github.com/FowwazM/repo_name](https://github.com/FowwazM/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [AWS Introducing Generative AI Course](https://www.udacity.com/course/generative-AI-with-AWS--cd13232)
* [Markdown Badges](https://github.com/Ileriayo/markdown-badges?tab=readme-ov-file#markdown-badges)
* [Project Logo Icon](https://www.flaticon.com/free-icon/artificial-intelligence_2591910)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/FowwazM/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/FowwazM/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/FowwazM/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/FowwazM/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/FowwazM/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/FowwazM/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/FowwazM/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/FowwazM/repo_name/issues
[license-shield]: https://img.shields.io/github/license/FowwazM/repo_name.svg?label=license&style=for-the-badge
[license-url]: https://github.com/FowwazM/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/fowwaz-moeen/
[Sagemaker-Badge]: https://img.shields.io/badge/AWS%20Sagemaker-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white
[Sagemaker-url]: https://aws.amazon.com/sagemaker/
[Huggingface-Badge]: https://img.shields.io/badge/Hugging%20Face-FEAA2D?style=for-the-badge&logo=deezer&logoColor=white
[Huggingface-url]: https://huggingface.co
[Numpy-Badge]: https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white
[Numpy-url]: https://numpy.org/
[Pandas-Badge]: https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white
[Pandas-url]: https://pandas.pydata.org/