
FROM demisto/python3:3.8.3.8715

COPY requirements.txt .

RUN apk add --no-cache python3-dev libffi-dev gcc musl-dev make \
  && apk --update add --no-cache --virtual .build-dependencies python-dev build-base wget git \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
