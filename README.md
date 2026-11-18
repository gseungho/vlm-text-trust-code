# 이미지와 텍스트의 응답 비교 코드

상품 사진의 동일성 판단과 사진·캡션의 일치 여부를 비교하는 Python 패키지 `vtrust`입니다. 이미지 준비, 요청 구성, batch 실행·재개, 응답 추출과 통계 계산 코드를 담고 있습니다.

## 설치

Python 3.10 이상에서 설치합니다.

```sh
python -m pip install -e ".[dev,sample]"
```

## 테스트

```sh
python -m pytest
```

테스트는 가상의 문항·이미지와 모의 API 응답을 사용합니다. 실제 API를 호출할 때는 환경 변수 `KSYCO_ANTHROPIC_API_KEY`를 설정합니다.

## 코드 구성

- `src/vtrust/`: 이미지 준비, 조건별 요청 구성, batch 처리와 응답 분석
- `tests/`: 요청 구성과 분석 함수의 테스트

명령별 옵션은 다음과 같이 확인합니다.

```sh
python -m vtrust.run --help
python -m vtrust.caption_run --help
python -m vtrust.caption_sample --help
```

실행에 필요한 문항·이미지·설정 파일과 저장된 응답은 별도로 준비합니다. 코드 라이선스는 MIT이며, 전문은 [LICENSE](LICENSE)에 있습니다.
