### brew 설치 쉘 스크립트
	- 임시
		- hombrew
			- mas
				- kakao
			- google-chrome
			- iina
			- visual-studio-code
				- todo: code 명령어 설정 알아보기
			- keyboardcleantool
			- appcleaner
			- raycast
			- iterm2
				- ```shell
				  # oh-my-zsh
				  sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
				  
				  # 파일열기
				  vi ~/.zshrc
				  
				  # ZSH_THEME찾아서 아래 내용으로 수정
				  ZSH_THEME="agnoster"
				  
				  # 아래 내용 추가
				  # 컴퓨터 이름 제거
				  prompt_context() {
				      if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then
				        prompt_segment black default "%(!.%{%F{yellow}%}.)$USER"
				    fi
				  }
				  
				   
				  
				  ## 저장후 적용
				  source  ~/.zshrc
				  ```
				-
		-
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
	  	nvm
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