# Docker
> 도커 학습 관련 repo

## 기본 조작

### `sudo 입력하지 않기`
> docker 명령은 root 권한으로 실행해야 하기 때문에 일반 계정에서는 항상 sudo를 사용함.

- 위의 상황을 해결하는 방법은 2가지
    - root 계정 로그인
    ```console
    (base) minkj1992@minkj1992-900X5L:~$ sudo su
    ```
    - 현재 계정을 docker 그룹에 포함
        - docker 그룹은 root 권한과 동일하다
        - 다만 꼭 필요한 계정만 포함
    ```bash
    (base) minkj1992@minkj1992-900X5L:~$ sudo usermod -aG docker minkj1992
    (base) minkj1992@minkj1992-900X5L:~$ sudo service docker restart
    ```