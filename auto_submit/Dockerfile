# Copyright 2022 The Flutter Authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.


# Dart Docker official images can be found here: https://hub.docker.com/_/dart
FROM dart:beta@sha256:7fef8712c268d41081d36a58745872e527c387bf68cf0bbb86e912201e30f3bf

WORKDIR /app

# Copy app source code (except anything in .dockerignore).
COPY . .
RUN dart pub get

# Start server.
EXPOSE 8080
CMD ["/usr/lib/dart/bin/dart", "/app/bin/server.dart"]
