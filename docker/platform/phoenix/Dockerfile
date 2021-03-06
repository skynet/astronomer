#
# Copyright 2018 Astronomer Inc.
#
# Licensed under the Apache License, Version 3.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM astronomerinc/ap-base
MAINTAINER Astronomer <humans@astronomer.io>

ARG BUILD_NUMBER=-1
LABEL io.astronomer.docker.build.number=$BUILD_NUMBER
LABEL io.astronomer.docker.module="astronomer"
LABEL io.astronomer.docker.component="phoenix"

ARG VERSION="0.0.11"
ENV REPO="github.com/astronomerio/phoenix"
ENV REPO_URL="https://${REPO}"

ENV GIN_MODE=release

WORKDIR /usr/lib/go/src/${REPO}

RUN apk add --no-cache --virtual .build-deps \
		build-base \
		git \
		go \
	&& git clone \
		-c advice.detachedHead=false \
		--depth 1 \
		--branch ${VERSION} \
		${REPO_URL} . \
	&& make DESTDIR=/usr/bin install \
	&& rm -rf /usr/lib/go \
	&& apk del .build-deps

ENTRYPOINT ["phoenix"]
