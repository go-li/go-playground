# Copyright 2014 The Go Authors.  All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM mysandbox

# add dir for gccgo
RUN mkdir -p /opt

# add gccgo from /opt
ADD gccgo.tar.bz2 /opt

# add and compile sandbox daemon
COPY . /go/src/gccbox
RUN go install gccbox


EXPOSE 8078
ENTRYPOINT ["/go/bin/gccbox"]
