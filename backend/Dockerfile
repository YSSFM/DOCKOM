FROM python:3.10-slim 

WORKDIR /app 

COPY requirements.txt . 
RUN pip install --no-cache-dir \
    --timeout 300 --retries 10 \
    -i https://pypi.tuna.tsinghua.edu.cn/simple \
    --trusted-host pypi.tuna.tsinghua.edu.cn \
    -r requirements.txt

COPY . . 

CMD ["python", "app.py"] 