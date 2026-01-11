# PDF Toolkit 개발 로그

## 세션 날짜: 2026-01-10

---

## 작업 내용

### 1. 컬러 스킴 변경 (Sunset Coral → Ocean Blue)

**문제**: 기존 Sunset Coral 테마가 "bloody"한 느낌 (빨간색이 너무 강함)

**제안한 대안 옵션**:
1. Electric Purple (#a855f7, #ec4899)
2. Ocean Blue (#3b82f6, #06b6d4) ✅ 선택됨
3. Mint Fresh (#10b981, #34d399)
4. Golden Hour (#f59e0b, #fbbf24)
5. Aurora Violet (#8b5cf6, #06b6d4)

**적용된 변경사항**:

| 요소 | 이전 (Sunset Coral) | 이후 (Ocean Blue) |
|------|---------------------|-------------------|
| 메인 포인트 컬러 | #ff6b6b (코랄) | #3b82f6 (블루) |
| 서브 포인트 컬러 | #feca57 (골드) | #06b6d4 (시안) |
| 배경 힌트 | #1a0a0a (다크레드) | #0a0a1a (다크블루) |
| 모달 배경 | #1a0f0f | #0f0f1a |
| 드롭존 테두리 | #3d2a2a | #2a2a3d |
| RGBA 글로우 | rgba(255, 107, 107, x) | rgba(59, 130, 246, x) |

**제목 그라데이션**:
```css
/* 이전 */
background: linear-gradient(135deg, #ff6b6b 0%, #feca57 50%, #ff9ff3 100%);

/* 이후 */
background: linear-gradient(135deg, #3b82f6 0%, #06b6d4 50%, #8b5cf6 100%);
```

---

## PDF Toolkit 전체 기능 목록 (17개)

### 변환 (Convert)
- PDF to Images - PDF를 PNG/JPG로 변환
- Images to PDF - 이미지를 PDF로 변환
- PDF to Text - 텍스트 추출
- PDF to Grayscale - 흑백 변환

### 편집 (Edit)
- PDF Merge - PDF 합치기
- PDF Split - PDF 분할
- PDF Rotate - 페이지 회전
- PDF Page Reorder - 순서 변경
- PDF Add Pages - 페이지 삽입
- PDF Remove Pages - 페이지 삭제
- PDF Watermark - 워터마크

### 최적화 (Optimize)
- PDF Compressor - 용량 감소
- PDF Optimizer - 웹 최적화

### 보안 (Security)
- PDF Protect - 비밀번호 설정
- PDF Unlock - 비밀번호 제거

### 정보 (Info)
- PDF Metadata - 메타데이터 보기
- PDF Page Count - 페이지 수 확인

---

## 수정된 파일

```
C:/Users/A/Desktop/lab/claude_lab/pdf to png/index.html
```

---

## 사용된 라이브러리

- **PDF.js** (Mozilla) - PDF 렌더링 및 파싱
- **pdf-lib** - PDF 생성 및 편집
- **JSZip** - ZIP 파일 생성 (다중 이미지 다운로드)

---

## 상태

✅ Ocean Blue 테마 적용 완료
✅ 17개 기능 모두 구현됨
