# EKAYA VS Code 확장 — 배포

EKAYA VS Code 확장의 **`.vsix` 배포 전용 레포**입니다. 소스는 공개하지 않습니다.

받을 곳은 [Releases](https://github.com/ekaya-labs/ekaya-vscode-release/releases) 입니다.

## 확장

| 확장 | 하는 일 |
| --- | --- |
| `ekaya-hub` | 액티비티 바의 **EKAYA 컨테이너**를 선언합니다. 코드가 없고 단독으로는 아무 기능도 하지 않습니다. |
| `ekaya-tasks` | 워크스페이스 태스크를 아이콘 목록으로 띄우고 한 번 클릭으로 실행합니다. |

## 설치

**`hub`를 먼저 설치해야 합니다.** 다른 확장들은 자기 아이콘을 만들지 않고 `hub`가 만든
컨테이너에 뷰만 꽂기 때문에, `hub`가 없으면 설치가 거부됩니다. 액티비티 바 아이콘을
하나로 유지하기 위한 구조입니다.

```sh
code --install-extension hub.vsix
code --install-extension tasks.vsix
```

또는 VS Code에서 `Ctrl+Shift+P` → `Extensions: Install from VSIX...` 를 같은 순서로 두 번.

## 릴리스 태그

확장마다 버전과 태그가 독립입니다.

```
tasks/v0.1.0
```

`hub`는 아이콘이나 제목을 바꾸지 않는 한 버전이 오르지 않으므로, 대개 릴리스마다
같은 `hub.vsix`가 함께 올라갑니다.

## 이슈

버그와 요청은 이 레포의 [Issues](https://github.com/ekaya-labs/ekaya-vscode-release/issues)로 받습니다.

목록이 비어 보인다면, 먼저 출력 패널(`Ctrl+Shift+U`)의 **EKAYA Tasks** 채널을 확인하고
그 내용을 함께 적어주세요. 열린 워크스페이스 폴더와 찾은 태스크 개수가 남습니다.
