# 3scale-pipeline-demo

# Prerequisites

1. Install 3scale-toolbox.

  a. Install Ruby
  
  ```
  sudo yum install git-core zlib zlib-devel gcc-c++ patch readline readline-devel libyaml-devel libffi-devel openssl-devel make bzip2 autoconf automake libtool bison curl sqlite-devel
  
  curl -sL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-installer | bash -
  
  echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
  echo 'eval "$(rbenv init -)"' >> ~/.bashrc
  source ~/.bashrc
  
  rbenv install 2.5.1
  rbenv global 2.5.1
  
  ruby -v
  ```
  
  b. Install 3scale-toolbix
  
  ```
  gem install 3scale_toolbox
  
  ```
  
  2. Install Jenkins on Openshift
  ```
  oc new-app jenkins-ephemeral
  ```
  
  # Pipeline Demo
  
  ```
  oc apply -f 3scale-build-pipeline.yaml
  
  ```
  Above command creates BuildConfig object in Openshift.
  
  Start the build
  
