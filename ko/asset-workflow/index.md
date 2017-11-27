# 에셋 작업흐름(Asset workflow)

## 에셋 추가(Adding an asset)

에셋을 프로젝트에 추가하는 방법은 세 가지가 있습니다:

* **create** 버튼을 사용하여 에셋 추가
* 운영 체제 파일 관리자에서 에셋 파일을 프로젝트 에셋 폴더로 복사 한 다음 코코스 생성기 창을 다시 열거나 새로고침하여 에섯 가져오기를 완료합니다.
* 에셋 파일을 운영 체제 파일 관리자(Windows의 탐색기 또는 Mac OS의 Finder)에서 **assets** 패널로 드래그하여 에셋을 가져옵니다.


### 외부에서 에섯 가져오기(Importing an asset from outside)
외부에서 에셋을 가져 오려면 운영 체제의 다른 창에서 파일을 코코스 창에있는 **assets** 패널로 드래그 & 드롭할 수 있습니다. 이 작업은 에셋 파일을 프로젝트 에셋 파일로 자동 복사하고 가져오기 작업을 완료합니다.

## Importing and synchronizing assets
**assets**의 에셋과 파일 관리자에 표시된 프로젝트 에셋 파일은 동기화됩니다. **assets**에서 에셋을 이동, 이름 바꾸기 및 삭제하면 사용자 파일 시스템의 에셋 파일과 동일한 변경이 수행됩니다. 마찬가지로 파일 시스템에서 에셋을 추가 또는 삭제 한 후(예:Windows의 탐색기 또는 Mac OS의 Finder) 코코스 프로그램을 다시 열거나 새로고침하면 **assets**의 에셋이 업데이트됩니다.

## 에셋 메타 파일 관리(Managing Asset Meta Files)

에셋 파일을 `assets` 폴더에 임포트할 때, 같은 위치에 동일한 파일 이름을 가진 **Meta file**이 생성됩니다. 이 메타 파일에는 에셋의 유니버설 고유 ID(uuid)와 텍스처의 잘라내기 정보와 같은 기타 중요한 설정이 포함됩니다.

코코스 크리에이터에서 에셋을 관리 할 때 메타 파일은 숨겨져 자동으로 처리됩니다. 즉 에셋 삭제, 이름 바꾸기, 이동하는 경우 해당 메타 파일이 삭제되고 이름이 바뀌며 그에 따라 이동됩니다.

** 탐색기 및 Finder와 같은 OS 파일 시스템에서 에셋을 관리하려고하면 삭제, 이름 바꾸기 및 이동과 같이 메타 파일을 수동으로 업데이트해야합니다.**

### 매칭되지 않는 에셋 메타 처리(Handling Unmatched Asset Meta)

경고 : 일치하지 않는 에셋 메타가 발견되었습니다.

메타 파일을 이동하거나 이름을 변경하지 않고 Explorer 또는 Finder에서 에셋 파일을 이동하거나 이름을 바꾼 경우 에디터는 이동되거나 이름이 변경된 에셋을 새로 가져온 것으로 간주하여 새로운 uuid로 새 메타 파일을 만듭니다. 또한 이전 메타 파일에는 일치하는 에셋은 제거됩니다. 또한 씬 및 컴포넌트의 에셋(스크립트 포함)에 대한 잘못된 참조를 유발합니다.

그런 일이 발생하면 에디터는 사용자에게 다음과 같은 경고 메시지를 표시합니다.

(스크린샷)

일치하지 않는 메타 파일은 `assets` 폴더에서 제거되고 `temp` 폴더에 백업됩니다.

변경된 참조를 복구하려면 백업 메타 파일을 변경된 에셋과 동일한 폴더에 넣고 변경된 에셋과 이름이 같은 메타 파일의 이름을 변경해야합니다. 변경된 에셋에 대해 새 메타 파일이 생성되어있을 가능성이 높기 때문에 백업 메타 파일을 복구 한 후에 새로 만든 메타 파일을 삭제할 수 있습니다.

## 프로젝트간 에셋 이전(Export assets from one project to another)

v1.5부터 코코스 크리에이터는 사용자가 하나의 프로젝트에서 다른 프로젝트로 에셋을 이전할 수 있게 합니다. [프로젝트간에 자산 가져오기/내보내기](import-export.md)를 읽으십시오.

## 다른 에디터에서 프로젝트 가져오기(Importing projects from other Editors)

이제 다른 에디터의 프로젝트를 가져올 수 있습니다. 자세한 내용은 다음을 참조하십시오 : [다른 에디터에서 프로젝트 가져오기](project-import.md)

## 일반 에셋 작업흐름(Common asset workflow)
다음으로 코코스 크리에이터의 주요 에셋 유형과 관련 작업흐름을 소개합니다:

- [씬 에셋(Scene asset)](scene-managing.md)
- [이미지 에셋(Image asset)](sprite.md)
- [아틀라스(Atlas)](atlas.md)
- [오토아틀라스 에셋(Auto-atlas asset)](auto-atlas.md)
- [스프라이트프레임을 위한 자동 자르기(Auto Trim for SpriteFrame)](trim.md)
- [스크립트 에셋(Script asset)](script.md)
- [폰트 에셋(Font asset)](font.md)
- [파티클 에셋(Particle asset)](particle.md)
- [오디오 에셋(Audio asset)](audio-asset.md)
- [프리펩(Prefab)](prefab.md)
- [스파인(Spine)](spine.md)
- [타일맵(TiledMap)](tiledmap.md)
- [드래곤본(DragonBones)](dragonbones.md)

---

계속해서 [씬 생성 및 관리(Create and Manage Scenes)](scene-managing.md)에 대해 알아보세요.
