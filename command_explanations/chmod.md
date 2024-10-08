# chmod 명령어 상세 설명

`chmod`는 "change mode"의 약자로, 파일이나 디렉토리의 권한을 변경하는 리눅스 명령어입니다.

## 기본 사용법

```bash
chmod [옵션] 모드 파일명
```

## 권한 설정 방식

1. 심볼릭 모드
   - 형식: `chmod [u/g/o/a][+/-/=][rwx] 파일명`
   - 예: `chmod u+x script.sh` (소유자에게 실행 권한 추가)

2. 숫자 모드
   - 형식: `chmod xyz 파일명` (x, y, z는 0-7 사이의 숫자)
   - 예: `chmod 755 script.sh` (소유자 모든 권한, 그룹과 기타 사용자 읽기/실행 권한)

## 숫자 모드 계산 방법

- 4: 읽기 권한
- 2: 쓰기 권한
- 1: 실행 권한

이들을 조합하여 원하는 권한을 설정합니다. 
예: 7 = 4 + 2 + 1 (읽기 + 쓰기 + 실행)

## 실습 예제

```bash
# 모든 사용자에게 실행 권한 추가
chmod +x test_script.sh

# 소유자에게 모든 권한, 그룹과 기타 사용자에게 읽기와 실행 권한 부여
chmod 755 test_script.sh
```

chmod 명령어를 이해하고 사용하는 것은 리눅스 파일 시스템 보안과 관리에 매우 중요합니다.