
FROM demisto/pyjwt3:1.0.0.8871

COPY requirements.txt .

RUN apk add --no-cache python3-dev libffi-dev gcc musl-dev make \
  && apk --update add --no-cache --virtual .build-dependencies python-dev build-base wget git \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
