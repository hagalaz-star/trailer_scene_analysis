# trailer_scene_analysis


- 데이터: 영화 예고편 5편(Arrival, Blade Runner 2049, Dune: Part Three, Interstellar, Tenet)
- PySceneDetect로 장면 분할해 만든 키프레임 450장 (영상 파일은 저장소에 포함하지 않음)

- 모델: CLIP ViT-B/32로 이미지·텍스트를 512차원 벡터로 변환

- 검색: FAISS(Inner Product, 정규화 벡터 = 코사인 유사도)
  - 이미지 → 이미지, 영화 간 유사 장면, 텍스트 → 이미지 검색
  - `max_per_movie`로 한 영화에 결과가 몰리는 것 제한

- 시각화: UMAP + Gradio로 임베딩 분포 확인
