park_python => requirements.txt에 mysqlclient==2.2.4
parking bot entry/exit 분리

settings.py 수정 (mariadb에 맞게)



backend deployment => 좀 더 널널하게


# 예시: Deployment.yaml
livenessProbe:
  httpGet:
    path: /api/health/db/
    port: 8000
  initialDelaySeconds: 30  # 앱이 뜨는 시간을 기다려줌 (30초로 증설)
  periodSeconds: 15        # 체크 간격
  timeoutSeconds: 5        # 응답 대기 시간 (5초로 증설)
  failureThreshold: 3      # 3번 실패하면 재시작 
