Run with openai

docker run -it --pull=always --rm -e PERSIST_SANDBOX="true" -e SSH_PASSWORD="supercoolsafepwd252352" -e LLM_BASE_URL="https://api.openai.com/v1" -e LLM_MODEL="gpt-4o" -e AGENT="CodeActAgent" -e LANGUAGE="en" -e LLM_API_KEY='sk-openaiApiKey' -e SANDBOX_ENV_GITHUB_TOKEN='ghp_token' -e SANDBOX_USER_ID='1111' -e WORKSPACE_MOUNT_PATH='C:\\Users\\User\\opendevin' -v /var/run/docker.sock:/var/run/docker.sock -v 'C:\\Users\\User\\opendevin:/opt/workspace_base' -p 3000:3000 --add-host host.docker.internal:host-gateway --name opendevin ghcr.io/opendevin/opendevin:main

Run with ollama
docker run -it --pull=always --rm -e PERSIST_SANDBOX="true" -e SSH_PASSWORD="supercoolsafepwd252352" -e LLM_BASE_URL="http://host.docker.internal:11434" -e LLM_MODEL="ollama/codestral:latest" -e AGENT="CodeActAgent" -e LANGUAGE="en" -e LLM_API_KEY="ollama" -e SANDBOX_ENV_GITHUB_TOKEN='ghp_token' -e SANDBOX_USER_ID='1111' -e WORKSPACE_MOUNT_PATH='C:\\Users\\User\\opendevin' -v /var/run/docker.sock:/var/run/docker.sock -v 'C:\\Users\\User\\opendevin:/opt/workspace_base' -p 3000:3000 --add-host host.docker.internal:host-gateway --name opendevin ghcr.io/opendevin/opendevin:main

