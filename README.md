# Exported from Render
version: "1"
services:
  - type: web
    name: n8n-service
    env: docker
    plan: free
    autoDeploy: true
    dockerfilePath: Dockerfile
    envVars:
      - key: N8N_BASIC_AUTH_ACTIVE
        value: "true"
      - key: N8N_BASIC_AUTH_USER
        value: "admin"
      - key: N8N_BASIC_AUTH_PASSWORD
        value: "rahasia123"
      - key: N8N_HOST
        value: eradealer-n8n.onrender.com
      - key: N8N_PORT
        value: "443"
      - key: DB_TYPE
        value: postgresdb
      - key: DB_POSTGRESDB_DATABASE
        value: n8n
      - key: DB_POSTGRESDB_USER
        value: render
      - key: DB_POSTGRESDB_PASSWORD
        value: ${DB_POSTGRESDB_PASSWORD}
      - key: DB_POSTGRESDB_HOST
        value: ${DB_POSTGRESDB_HOST}
      - key: DB_POSTGRESDB_PORT
        value: ${DB_POSTGRESDB_PORT}

databases:
  - name: n8n-db
    plan: free
