# wanted-pre-onboarding-challenge-fe-2
  # 안녕하세요 
퍼블리셔에서 프론트엔드로 이직을 준비중입니다. 
프리온 보딩에서 타입스크립트를 배운다는 좋은 소식이 있어 신청했습니다. 
배워보지 않은 영역이지만, 사전과제부터 흥미가 쏠쏠하네요.

## 챌린지 과제 가이드

>요구 사항을 구현하지 않고 설계만합니다.
- 모든 요구사항은 JSDoc을 기반으로 수행합니다.
- Todo 앱을 JSDoc으로 합니다.
- Public으로 완성한 과제를 모집 마감 후 설문 조사를 통해 제출해주세요. (개강 시 설문 조사 링크 전달 예정)
- 제출할 저장소 명은 wanted-pre-onboarding-challenge-fe-2로 생성해 주세요.
- 과제 수행 개수에 따라 기본적인 평가가 이루어지며, 커리큘럼 운영 과정에서 최소한의 수준을 파악하기 위한 용도입니다.
- 해당 과제에 대한 해설은 개강 후 진행될 예정입니다.
- README.md를 꼭 작성해 주세요. 본인에 대한 소개나 프로젝트 소개 등 자유롭게 작성해주시면 됩니다.


## 📝 Requirements

### 필수 요구사항
>아래의 Todo 앱 요구사항을 참고하여
- 필요한 데이터를 모두 모델링한다.
- 사용되는 모든 함수를 `선언부만` 만든다.
  - 함수 및 클래스의 내부는 구현하지 않습니다.
- `JSDoc`을 활용해 문서화한다.
- `GitHub Page`를 활용해 `JSDoc` 정적 페이지를 배포한다.

### Todo

```js
Todo {
  아이디(required),
  내용(required),
  완료여부(required),
  카테고리(required),
  태그들(optional),
}
```

#### CREATE

- 할 일을 추가할 수 있다.
- 내용없이 추가할 수 없다.

#### READ

- 모든 할 일을 조회할 수 있다.
- ID를 기반으로 특정 할 일을 조회할 수 있다.

#### UPDATE

- ID를 제외한 모든 속성을 수정할 수 있다.
- 특정 할 일의 특정 태그를 수정할 수 있다.

#### DELETE

- ID를 기반으로 특정 할 일을 삭제할 수 있다.
- 모든 할 일을 제거할 수 있다.
- 특정 할 일의 특정 태그를 삭제할 수 있다.
- 특정 할 일의 모든 태그를 제거할 수 있다.


#### Modeling (Shape)

```js
Item {
  property(required),
  property(optional),
}
```

#### Reference

- [use JSDoc](https://jsdoc.app)
- [JSDoc Boilerplate](https://github.com/pocojang/jsdoc-boilerplate)
# JSDoc

[![Build Status](https://travis-ci.org/jsdoc/jsdoc.svg?branch=master)](http://travis-ci.org/jsdoc/jsdoc)

An API documentation generator for JavaScript.

Want to contribute to JSDoc? Please read `CONTRIBUTING.md`.

Installation and Usage
----------------------

JSDoc supports stable versions of Node.js 8.15.0 and later. You can install
JSDoc globally or in your project's `node_modules` folder.

To install the latest version on npm globally (might require `sudo`;
[learn how to fix this](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally)):

    npm install -g jsdoc

To install the latest version on npm locally and save it in your package's
`package.json` file:

    npm install --save-dev jsdoc

**Note**: By default, npm adds your package using the caret operator in front of
the version number (for example, `^3.6.3`). We recommend using the tilde
operator instead (for example, `~3.6.3`), which limits updates to the most
recent patch-level version. See
[this Stack Overflow answer](https://stackoverflow.com/questions/22343224) for
more information about the caret and tilde operators.

To install the latest development version locally, without updating your
project's `package.json` file:

    npm install git+https://github.com/jsdoc/jsdoc.git

If you installed JSDoc locally, the JSDoc command-line tool is available in
`./node_modules/.bin`. To generate documentation for the file
`yourJavaScriptFile.js`:

    ./node_modules/.bin/jsdoc yourJavaScriptFile.js

If you installed JSDoc globally, run the `jsdoc` command:

    jsdoc yourJavaScriptFile.js

By default, the generated documentation is saved in a directory named `out`. You
can use the `--destination` (`-d`) option to specify another directory.

Run `jsdoc --help` for a complete list of command-line options.

## Templates and tools

The JSDoc community has created templates and other tools to help you generate
and customize your documentation. Here are a few of them:

### Templates

+ [jaguarjs-jsdoc](https://github.com/davidshimjs/jaguarjs-jsdoc)
+ [DocStrap](https://github.com/docstrap/docstrap)
([example](https://docstrap.github.io/docstrap))
+ [jsdoc3Template](https://github.com/DBCDK/jsdoc3Template)
  ([example](https://github.com/danyg/jsdoc3Template/wiki#wiki-screenshots))
+ [minami](https://github.com/Nijikokun/minami)
+ [docdash](https://github.com/clenemt/docdash)
([example](http://clenemt.github.io/docdash/))
+ [tui-jsdoc-template](https://github.com/nhnent/tui.jsdoc-template)
([example](https://nhnent.github.io/tui.jsdoc-template/latest/))
+ [better-docs](https://github.com/SoftwareBrothers/better-docs)
([example](https://softwarebrothers.github.io/admin-bro-dev/index.html))

### Build tools

+ [JSDoc Grunt plugin](https://github.com/krampstudio/grunt-jsdoc)
+ [JSDoc Gulp plugin](https://github.com/mlucool/gulp-jsdoc3)

### Other tools

+ [jsdoc-to-markdown](https://github.com/jsdoc2md/jsdoc-to-markdown)
+ [Integrating GitBook with
JSDoc](https://medium.com/@kevinast/integrate-gitbook-jsdoc-974be8df6fb3)

## For more information

+ Documentation is available at [jsdoc.app](https://jsdoc.app/).
+ Contribute to the docs at
[jsdoc/jsdoc.github.io](https://github.com/jsdoc/jsdoc.github.io).
+ [Join JSDoc's Slack channel](https://jsdoc-slack.appspot.com/).
+ Ask for help on the
[JSDoc Users mailing list](http://groups.google.com/group/jsdoc-users).
+ Post questions tagged `jsdoc` to
[Stack Overflow](http://stackoverflow.com/questions/tagged/jsdoc).

## License

JSDoc 3 is copyright (c) 2011-present Michael Mathews <micmath@gmail.com> and
the [contributors to JSDoc](https://github.com/jsdoc/jsdoc/graphs/contributors).

JSDoc 3 is free software, licensed under the Apache License, Version 2.0. See
the file `LICENSE.md` in this distribution for more details.


{
  "plugins": ["node_modules/jsdoc/plugins/markdown"], // Markdown을 사용하기 위해 플러그인을 추가합니다.
  "recurseDepth": 10, // -r 명령 행 플래그로 재귀가 사용 가능한 경우 JSDoc은 10 레벨 깊이의 파일을 검색합니다.
  "source": {
    "include": ["./"],	// ./에 includepattern에 해당하는 파일을 대상으로 함
    "includePattern": ".+\\.js(x|doc)?$", // js, jsx, jsdoc 이라는 확장자를 가진 것을 Docs로 변환합니다.
    "excludePattern": "(^|\\/|\\\\)_" // 밑줄로 시작하거나 밑줄로 시작하는 디렉토리에있는 모든 파일은 무시됩니다.
  },
  "sourceType": "module", // ES 2015를 지원하기 위해 적용
  "tags": {
    "allowUnknownTags": true // JSDoc이 알 수 없는 태그를 지원하도록 설정
  },
  "opts": {
    "encoding": "utf8", // Docs에서 한글을 사용할 수 있도록 설정
    "destination": "./docs" // 기존에 생성되던 out이라는 폴더를 docs라는 폴더로 생성
    "readme": "README.md",  // README.md를 추가
  }
}
