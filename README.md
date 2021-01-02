# helm-repo
쿠버네티스 패키지 관리 도구인 helm의 repository입니다.

## helm repo 추가

```bash
helm repo add choshsh https://shsteak.github.io/helm-repo/
```

## 확인

```bash
helm repo update && helm search repo choshsh
```

## 패키지 사용법

- pull

    ```bash
    helm pull choshsh/<차트>
    ```

- install
    1. 테스트 및 결과물 확인

        ```bash
        helm install choshsh/<차트명> --generate-name --dry-run --debug
        ```

    2. 실행

        ```bash
        helm install choshsh/jenkins --generate-name
        ```

        - 옵션

            `--namespace` : namespace 설정

            `--name-template` : Alias 설정 (Deployment, Service, Pod 등에 영향을 준다)

            `--set` : values 설정 (yaml파일 / String)
