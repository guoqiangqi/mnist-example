FROM alpine/git:v2.32.0
RUN git clone https://github.com/guoqiangqi/mnist-example.git /mnist-example

FROM python:3.8.12-slim-buster
# RUN apk add g++
RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple tensorflow

COPY --from=0 /mninst-example /mnist-example
WORKDIR /mnist-example
CMD ["IS_TRAIN=True python", "mnist_train_eval.py"]
