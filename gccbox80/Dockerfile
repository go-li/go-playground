# Copyright 2014 The Go Authors.  All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM go-playground-sandbox80

# add dir for gccgo
RUN mkdir -p /opt

# add gccgo from /opt
RUN curl https://docs.google.com/uc?export=download&confirm=o-9b&id=0BwW7BsjjnpjFQVV3T09oMHd5UVU | tar -xz -C /opt

# add and compile sandbox daemon
COPY . /go/src/gccbox
RUN go install gccbox


EXPOSE 80
ENTRYPOINT ["/go/bin/gccbox"]
