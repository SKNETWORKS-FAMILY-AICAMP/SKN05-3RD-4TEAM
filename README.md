# SKN05-3ST-4TEAM

### 3차 프로젝트: LLM을 연동한 내외부 문서 기반 질의응답 시스템<br>
 **개발기간: 2024.11.26-11.27**

-----

# 🤦‍♂️팀원

|  **이준호** |  **신혜원** |  **윤상혁** |  **배윤관** |
|:---------:|:---------:|:---------:|:-----------:|
| @Lanvizu | @gjslqjxjclq | @ggreing |  @yoonkwan95 |


# 💻문서 Q&A 시스템

## 프로젝트 개요

본 프로젝트는 다양한 문서의 내용을 효율적으로 파악하고 검색할 수 있는 AI 기반 문서 Q&A 시스템입니다. 

기존의 문서 검색 방식의 한계를 극복하고, 사용자가 원하는 정보를 쉽고 빠르게 얻을 수 있도록 설계했습니다.

## 주요 기능

- **문서 업로드 및 처리**: PDF, CSV, TXT, XLSX 등 다양한 형식의 문서를 업로드하고 처리할 수 있습니다.

- **AI 기반 문서 분석**: 업로드된 문서는 OpenAI의 임베딩 모델을 통해 분석되어 Pinecone 인덱스에 검색 가능한 형태로 저장됩니다.

- **자연어 질의응답**: 사용자는 일상적인 언어로 질문을 입력하고, GPT 모델을 활용하여 관련된 정보를 찾아 답변을 생성합니다.

- **검색 결과 제공**: 답변과 함께 참고한 문서의 출처와 관련 내용을 제공합니다.

- **실시간 처리**: Streamlit을 이용한 대화형 인터페이스로 실시간 질의응답이 가능합니다.

## 📜기술 스택

- **임베딩**: OpenAI의 text-embedding-ada-002 모델
- **벡터 검색**: Pinecone
- **자연어 생성**: GPT-3.5 또는 GPT-4 (OpenAI)
- **프론트엔드**: Streamlit
- **백엔드**: Python

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-0.3.7-orange)
![Pinecone](https://img.shields.io/badge/Pinecone-Vector%20DB-0091FF?style=flat&logo=pinecone&logoColor=white)
![OpenAI GPT-3.5 turbo](https://img.shields.io/badge/OpenAI-GPT--3.5--turbo-blueviolet?logo=openai&logoColor=white)
![OpenAI GPT-4](https://img.shields.io/badge/OpenAI-GPT--4-blueviolet?logo=openai&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.39.0-red?logo=streamlit&logoColor=white)

## 주요 컴포넌트

### text-embedding-ada-002

- **긴 문서 처리 용이성**: 최대 8192 토큰의 컨텍스트 길이를 지원해 다양한 길이의 문서 처리 가능
  
- **효율적인 임베딩 크기**: 이전 모델(davinci-001)에 비해 1/8 크기의 임베딩을 생성하여 저장 공간 및 처리 시간 절약

- **다국어 지원**: 여러 언어에 대한 임베딩을 생성할 수 있어 다양한 언어로 된 문서를 처리 가능
  
- **비용 효율성**: text-embedding-3-large 모델에 비해 더 저렴한 가격으로 프로젝트의 비용 관리에 용이

### Pinecone

- 실시간 벡터 데이터 처리 및 검색
  
- 높은 확장성으로 대용량 데이터 처리 가능
  
- OpenAI, LangChain 등과의 원활한 통합
  
- 초당 수십억 개의 항목을 검색할 수 있으며, 지연 속도가 50ms 미만으로 매우 빠른 응답 시간을 제공

### OpenAI GPT 모델

- 고성능 자연어 처리 및 생성 기능 제공
  
- 다양한 도메인에 적용 가능한 범용성
  
- Fine-tuning 없이도 높은 성능 발휘

## 시스템 아키텍처

1. **문서 업로드**: 사용자가 다양한 형식의 문서를 업로드합니다.

2. **텍스트 추출**: 업로드된 문서에서 텍스트를 추출합니다.

3. **텍스트 분할**: 추출된 텍스트를 적절한 크기로 분할합니다.

4. **임베딩 생성**: 분할된 텍스트를 OpenAI의 임베딩 모델을 사용해 벡터화합니다.

5. **벡터 저장**: 생성된 벡터를 Pinecone 인덱스에 저장합니다.

6. **질의 처리**: 사용자의 질문을 받아 관련 문서를 검색합니다.

7. **답변 생성**: 검색된 문서를 바탕으로 GPT 모델이 답변을 생성합니다.

## Streanlit 화면

![image](https://github.com/user-attachments/assets/42bb4a59-d59c-432d-85a2-febb792141b0)

![image](https://github.com/user-attachments/assets/fb894d6c-3bf4-4fce-b544-20203bc9a067)

## 사용 방법

1. 사이드바에서 문서를 업로드합니다.

2. "파일 처리 및 업로드" 버튼을 클릭하여 문서를 시스템에 등록합니다.

3. 채팅 인터페이스에 질문을 입력합니다.

4. 시스템이 관련 정보를 검색하고 답변을 생성합니다.

5. 답변과 함께 참고한 문서의 출처가 표시됩니다.

## 개선점

## 한 줄 회고
<hr>
<blockquote>

•	이준호 :  <br>
•	신혜원 :  <br>
•	윤상혁 :  <br>
•	배윤관 :  <br>

</blockquote>
