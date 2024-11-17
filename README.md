# Youth Policy Chatbot

## Project Overview

The Youth Policy Chatbot is a real-time interactive chatbot service that recommends personalized youth policies based on user-provided information such as residence, age, and employment status. This project aims to help users easily understand complex policy information through continuous conversations and assist them in conveniently selecting policies that suit their needs.

The chatbot leverages youth policy data from [Ontong Youth](https://www.youthcenter.go.kr/main.do), the official e-government website of South Korea, to provide fast and tailored recommendations based on region, age, and personal circumstances. It also offers detailed policy information. With a Gradio interface, the chatbot can be easily accessed via a web browser, offering an intuitive and user-friendly conversational experience.

### Key Features

1. **Personalized Policy Recommendations**

    - Recommends the most relevant policies based on user-provided details such as residence, age, and employment status.
   
    - Provides comparisons between similar policies.

2. **Detailed Policy Information**
   
    - Answers user queries about specific policies, such as application periods, eligibility requirements, and necessary documentation, by retrieving relevant information from policy documents.

3. **Policy Terminology Explanations**

   - Offers additional explanations for difficult terms included in policy information.

## Project Structure

```
youth_policy
├─ chatbot.py
├─ data
│  ├─ chromadb.py
│  ├─ crawling_words.ipynb
│  ├─ layout_analyzer.py
│  └─ policy_crawling_and_attached_file_save.py
├─ download_db.py
├─ README.md
└─ requirements.txt
```

## Installation

1. **Clone the repository**:

    Clone the repository to your local machine using the following command:

    ```bash
    git clone https://github.com/junhyeok9/youth_policy.git
    ```


2. **Navigate to the project directory**:

    Move into the directory of the cloned repository:

    ```bash
    cd youth_policy
    ```

3. **Install the required packages**:

    Install all the dependencies listed in the ```requirements.txt``` file:

    ```bash
    pip install -r requirements.txt
    ```


## Usage

1. **Download the Chroma DB from Google Drive**:

    Run the ```download_db.py``` script to download the necessary database files.

    ```bash
    python download_db.py
    ```   

2. **Set up API keys in environment variables**:

    Rename the ```.env.example``` file to ```.env```, and add your API keys inside the file.

3. **Run the chatbot**:

    Start the chatbot by running the ```chatbot.py``` script.

    ```bash
    python chatbot.py
    ```

4. **Open the Gradio interface**:

    After running the chatbot, open the Gradio interface in your web browser by navigating to:

    ```
    http://127.0.0.1:7860
    ```

## Pipeline

![pipeline](https://github.com/user-attachments/assets/704f4174-3137-43c1-8555-04de8646358e)

## Example

![example](https://github.com/user-attachments/assets/06e4137f-2012-471d-a3df-2bf065eb4019)

## Authors

This project was created by the following contributors:

- **강민정** 

    - 고려대학교 통계학과 석사

    - 정책용어 크롤링

    - 프롬프트 엔지니어링을 통한 챗봇 성능 개선
    
    - 프로젝트 소개서 작성

- **원준혁**

    - 고려대학교 통계학과 석사

    - 정책정보 크롤링 및 정책 파일 저장
    
    - 크롤링 정보 데이터베이스 저장 및 chunking, embedding

    - 데모 실행 조정 및 비디오 제작

- **이세은**

    - 고려대학교 통계학과 학부

    - SMART-RAG 파이프라인 구축 및 챗봇 실행 코드 작성

    - Gradio를 통한 웹서비스 구현

    - Github repository 정리 및 readme.md 작성


