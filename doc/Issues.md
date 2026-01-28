<details>
  <summary><strong>260127</strong></summary>
  
- 관측된 에러:
```
UnidentifiedImageError: cannot identify image file '/content/test_image/TEST_088.mov'
```

- 해결방안
  1. 폴더명에 맞게 이미지, 비디오 파일 분리
  2. 추후 문자열 추출로 분기 로직 구현
</details>

<details>
  <summary><strong>260128</strong></summary>

- 관측된 에러 :
  ```
  FileNotFoundError: [Errno 2] No such file or directory: 'config/config.yaml'
  ```
- 원인 분석 : colab의 cwd는 "/content"로 실제 파일 위치를 가리키지 않음  

- 고려 사항:  
  1. colab 개발, local 테스트, docker 제출(심사)로 실행환경에 유연한 코드 필요
  2. 다른 파일 내에서도 재사용 가능

- 해결 방안:  
  그 파일이 있는 위치를 기준으로 경로 계산
  ```
  from pathlib import Path
import yaml

BASE_DIR = Path(__file__).resolve().parent
CFG_PATH = BASE_DIR / "config" / "config.yaml"

cfg = yaml.safe_load(open(CFG_PATH))
```

</details>
