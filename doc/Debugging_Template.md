# 딥러닝 디버깅 로그

> 목적: **학습 실패/성능 저하/불안정성**을 체계적으로 추적하고 재현 가능하게 해결

---

## 1. 이슈 개요

* **이슈 ID**:
* **문제 유형**: (학습 불가 / 수렴 안 됨 / 과적합 / 성능 급락 / NaN 발생 등)
* **발생 시점**: (초기 / 중반 / 후반 epoch)
* **심각도**: (Critical / Major / Minor)

---

## 2. 환경(Environment)

* **프레임워크**: (PyTorch / TensorFlow / JAX)
* **버전**:
* **하드웨어**: (CPU / GPU / TPU, VRAM)
* **CUDA / cuDNN**:
* **Seed 고정 여부**:

---

## 3. 데이터 점검(Data Check)

* **데이터 크기**:
* **Train/Val/Test 분리 방식**:
* **라벨 분포 불균형 여부**:
* **입력 범위 / 정규화**:
* **이상치 / 깨진 샘플**:

---

## 4. 증상(Symptoms)

* 학습 로그 요약:

  * Loss 추이:
  * Metric 추이:
* 관측된 에러:

```
RuntimeError / NaN / Inf / OOM 로그
```

---

## 5. 재현 방법(Reproduction)

1. 실행 커맨드:
2. 설정 파일:
3. 특정 조건:

---

## 6. 가설 수립(Hypotheses)

* 가설 1:
* 가설 2:

---

## 7. 원인 분석(Root Cause)

* 확인한 사실:
* 배제한 원인:
* 실제 원인:

---

## 8. 모델/학습 설정 점검

* **모델 구조**:
* **초기화 방식**:
* **Loss Function**:
* **Optimizer / LR**:
* **Batch Size**:
* **Regularization**:

---

## 9. 해결 방법(Fix)

* 수정 요약:
* 변경 파일/설정:

```diff
# 변경 전 / 변경 후
```

---

## 10. 검증(Verification)

* 재학습 결과:
* 성능 비교:
* 재현성 확인:

---

## 11. 회고 및 재발 방지

* 놓친 체크 포인트:
* 예방 조치:

  * 데이터 검증 스크립트
  * Gradient/Loss 모니터링
  * 실험 자동화

---

## 12. 참고 자료

* 논문 / 공식 문서:
* 실험 노트 링크:

---

## 태그

`#deep-learning` `#debugging` `#training-failure` `#nan`
