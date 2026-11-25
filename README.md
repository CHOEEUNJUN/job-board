# 채용공고 모아보기

학과 학생 취업지원용 채용공고 목록 페이지입니다. GitHub Pages로 공개합니다.

## 구조

- `index.html`: 공고 목록 화면 (검색, 지역·경력 필터, 원문 링크)
- `jobs.json`: 표시할 공고 데이터. 연구실 서버가 잡코리아 API로 받아서 이 파일을 갱신합니다.

API 호출은 잡코리아에 등록한 연구실 서버 IP에서만 합니다. 이 페이지는 서버가 만든 `jobs.json`만 읽고, **API 호출 주소(고유 링크)는 저장소에 절대 올리지 않습니다.**

## jobs.json 형식

```json
{
  "source": "잡코리아",
  "updated_at": "2026-11-25 09:00",
  "jobs": [
    {
      "title": "공고명",
      "company": "회사명",
      "job": "직무",
      "region": "서울",
      "career": "신입",
      "education": "대졸이상",
      "due": "2026-12-10",
      "url": "잡코리아 공고 원문 URL"
    }
  ]
}
```

## GitHub Pages 켜기

1. 이 파일들을 새 공개 저장소에 올립니다.
2. 저장소 Settings → Pages → Branch를 `main` / `(root)`로 저장합니다.
3. 잠시 후 `https://<아이디>.github.io/<저장소명>/` 주소가 생깁니다. 이 주소를 잡코리아 신청서의 사용처 URL로 적습니다.
