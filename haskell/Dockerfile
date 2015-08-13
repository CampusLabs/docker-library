FROM debian:jessie
RUN awk '$1 ~ "^deb" { $3 = $3 "-backports"; print; exit }' /etc/apt/sources.list > /etc/apt/sources.list.d/backports.list
RUN apt-get update && apt-get -y install \
    git \
    libgmp-dev \
    libpq-dev \
    postgresql
RUN apt-get -y install ghc cabal-install
ENV PATH=".cabal-sandbox/bin:$HOME/.cabal/bin:$PATH"
RUN cabal update
RUN for package in alex happy hlint pointfree pointful scan stylish-haskell; \
    do which $package || cabal install $package; \
    done
