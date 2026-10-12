# Session 12 - Ex1: CI Matrix (JDK 17 & 21)

## Muc tieu
Chay song song test tren JDK 17 va JDK 21 bang Matrix Strategy, co Gradle caching.

## Cau truc
- `src/.../hello/HelloService.java` + `HelloServiceTest.java`: test nhanh, chay xanh tren ca 2 JDK.
- `.github/workflows/ci-matrix.yml`: workflow chinh cua bai.

## Workflow
- Trigger: `push` vao `main`.
- Job `test-matrix` re nhanh thanh `test-matrix (17)` va `test-matrix (21)`.
- Dung `actions/setup-java@v5` voi `distribution: temurin`, `cache: gradle`.

## Kiem tra
1. Push len GitHub, mo tab **Actions**.
2. Xac nhan 2 sub-job chay song song va tich xanh.
3. Chup man hinh tab Actions de nop bai (ke ca `Test on Java 17/21`).

## Chay local
```bash
./gradlew test
```
