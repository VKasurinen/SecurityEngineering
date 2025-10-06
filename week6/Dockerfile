# 3a-------------------------------------------------------------

# before:

# FROM ubuntu:latest
# RUN apt-get update && apt-get install -y python3
# CMD ["python3"]

# after:

# FROM ubuntu:22.04

# RUN apt-get update && \
#     apt-get install -y --no-install-recommends python3 && \
#     rm -rf /var/lib/apt/lists/*

# CMD ["python3"]

# 3b  ----------------------------------------------------------- 

# before:

# FROM ubuntu:22.04

# RUN apt-get update && \
#     apt-get install -y --no-install-recommends python3 && \
#     rm -rf /var/lib/apt/lists/*

# CMD ["python3"]

# after:

FROM ubuntu:24.04

RUN apt-get update && \
    apt-get install -y --no-install-recommends python3 && \
    rm -rf /var/lib/apt/lists/*

CMD ["python3"]



