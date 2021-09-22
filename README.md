# test-s2i-maven-web-source

## OCP 적용

### APP 생성
```
oc new-app openshift/jboss-eap73-openjdk11-openshift:latest~https://github.com/ddakker/test-s2i-maven-web-source.git --name=eap73 --as-deployment-config=true
```

### 라우트 생성
```
oc expose svc/eap73 --name=eap73
```

### 접속 테스트
```
curl http://eap73-[NS].[APPS DOMAIN]
```
