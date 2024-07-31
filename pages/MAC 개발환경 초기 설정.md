### brew 설치 쉘 스크립트
	- ```shell
	  #!/bin/bash
	  
	  # 홈브루가 설치되어 있는지 확인
	  if command -v brew &> /dev/null; then
	      echo "홈브루가 이미 설치되어 있습니다."
	  else
	      # 홈브루 설치
	      /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
	      echo "홈브루가 설치되었습니다."
	  fi
	  
	  # 설치할 일반 패키지 리스트
	  PACKAGES=(
	      git
	      node
	      python
	      wget
	      zsh
	      # 추가로 설치하고 싶은 패키지를 여기에 추가하세요.
	  )
	  
	  # 설치할 cask 패키지 리스트
	  CASK_PACKAGES=(
	      google-chrome
	      visual-studio-code
	      dbeaver-community
	      postman
	      slack
	  )
	  
	  echo "설치할 일반 패키지 리스트: ${PACKAGES[@]}"
	  echo "설치할 cask 패키지 리스트: ${CASK_PACKAGES[@]}"
	  
	  # 일반 패키지 설치
	  for PACKAGE in "${PACKAGES[@]}"; do
	      brew install $PACKAGE
	  done
	  
	  # cask 패키지 설치
	  for CASK in "${CASK_PACKAGES[@]}"; do
	      brew install --cask $CASK
	  done
	  
	  echo "설치 완료!"
	  ```