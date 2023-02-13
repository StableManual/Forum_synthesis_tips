# 외국 합성 포럼에서의 팁들(번역됨)

## 올바른 모델/체크포인트 사용

사람들이 저지르는 가장 큰 실수 중 하나는 인페인팅이 아닌 모델을 사용하는 것입니다. 
Normal Stable Diffusion 모델은 새로운 것을 생성하기 때문에 생성할 때 원본 이미지에 대한 모든 정보를 날려버립니다. 
인페인팅 모델은 원본 이미지를 기억해 두면서 이미지 자료를 더 잘 생성합니다. 
이는 사실적인 합성 이미지를 만드는 데 매우 중요합니다.

어떤 모델을 사용하면 좋나요? 항상 더 좋게 나오는 것이 몇 가지가 있습니다.
여기에 내가 현재 사용하고 있는 몇 가지가 있으며 그에 대한 몇 가지 의견이 있습니다.

* URPM 인페인팅
   * URPM 인페인팅은 몸에 꽤 좋지만 모든 이미지의 사람에게 거대한 가슴을 주는 경향이 있습니다.
   * 링크: https://civitai.com/models/2661/uber-realistic-porn-merge-urrpm (인페인팅 모델을 선택해야 함)

* Galaxy 인페인팅 V3
   * 이것은 모든면에서 매우 좋습니다. URPM보다 원래 옷을 더 많이 보존하는 경향이 있을 수 있습니다.
   * 링크: https://civitai.com/models/5152/galaxytimemachines-inpainting-models (설치 참고 사항에 대한 설명을 반드시 읽으십시오)

* RealisticVision 인페인팅
   * 이것이 제가 기본적으로 쓰는게 되었습니다. 모든면에서 아주 좋습니다.
   * 링크: https://civitai.com/models/4201/realistic-vision-v13 (인페인팅 모델을 선택하고 설치 지침을 읽으십시오)

* StableDiffusion v1.5 인페인팅
   * 기본모델로 사용


## 이미지 준비
이미지 품질이 좋지 않은 경우도 괜찮습니다.
Stable Diffusion은 낮은 해상도에서 작동하기에 후반에 업스케일링과 같은 작업으로 품질을 향상할 수 있습니다. 
이미지 품질이 엄청나게 낮은 경우 작업하기 전에 720p(또는 하드웨어가 약 768x768에서 렌더링할 수 있는 경우 1080p)와 같은 것으로 업스케일링할 수 있습니다.

작업하기 전에 이미지에 할 수 있는 주요 작업은 이미지를 밝게 하는 것입니다.(때에 따라 필요없습니다!)
너무 어두우면 Stable Diffusion이 세부 사항을 파악하기 어려울 수 있습니다. 
따라서 이미지를 Photoshop으로 가져온 다음 Camera RAW를 사용하여 노출을 높이는 것이 도움이 될 수 있습니다. 
과다 노출된 이미지로 작업하는 경우 나중에 되돌아가기가 어려울 수 있으므로 너무 선넘지 마십시오.

많은 사람들이 사진을 StableDiffusion 넣기 전에 사진에 약간의 스케치를 하는 것을 좋아합니다.
살색을 선택하고 그것으로 몸을 칠하고 유두가 있어야 할 곳에 칠하는 것이 포함될 수 있습니다. 
일부는 자체 음영을 추가하기도 합니다. 나는 일반적으로 이것이 불필요하다는 것을 알았습니다. 
제가 그림을 못그려서 다른 분들이 더 좋은 결과를 얻으실 수 있을 것 같아요. 
때때로 도움이 되는 것은 밝은 색상을 낮추기 위해 포토샵과 같은 프로그람의 색상 혼합 모드나 살색 브러시로 옷(예: 핫 핑크 또는 청록색) 위에 페인팅하는 것입니다. 
이렇게 하면 이미지를 조금 더 보존할 수 있습니다. 그러나 나는 보통 이미지가 문제를 일으키는 경우에만 이 작업을 수행합니다. 나중에 설명하겠습니다.


## 원래 옷 보존하기
원래 옷의 일부를 보존하고 싶다면 괜찮습니다. 인물이 가디건이나 셔츠를 입고 있고 가슴을 약간 드려내려 할 때 
명심해야 할 몇 가지 사항.
* 어깨까지 마스킹을 해주세요.
* Stable Diffusion은 약간의 옷을 렌더링하는 경향이 있으므로 노출을 원하는 부위만 색칠하는 것보다 조금 더 마스킹해야 합니다.


## 프롬프트 및 도구
인물이 중간 사이즈의 가슴을 가지고 사실적인 피부를 원하면 'a ((naked)) woman with medium breasts'를 입력하고 'highly detailed skin, 8k, uhd' 등과 같은 항목을 입력하십시오. 
CFG를 4로 설정하면 자동으로 자연스럽게 처리합니다. 프롬프트에서 아주 최소한으로 프롬프트를 시작하고 점점 추가하여 결과를 구체화하십시오.


Stable Diffusion이 학습했던 연예인에 대해 잘 알고 있다면(혹은 비슷한 체형을 가진 연예인을 떠올릴 수도 있다), 
그 연예인 이름을 프롬프트에 던질 수도 있다. 
Stable diffusion은 그들의 일반적인 체형을 이해하는 것과 같다.

부정적인 프롬프트의 경우 일반적으로 다음과 같은 것을 씁니다.

---

"((woman, tattoos, b&w)), ((((big hands, un-detailed skin, semi-realistic, cgi, 3d, render, sketch, cartoon, drawing, anime)))), (((ugly mouth, ugly eyes, missing teeth, crooked teeth, close up, cropped, out of frame))), worst quality, low quality, jpeg artifacts, ugly, duplicate, morbid, mutilated, extra fingers, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, blurry, dehydrated, bad anatomy, bad proportions, extra limbs, cloned face, disfigured, gross proportions, malformed limbs, missing arms, missing legs, extra arms, extra legs, fused fingers, too many fingers, long neck, huge breasts, fake breasts, breast implants, anorexic, emaciated,, long hair, chubby"

---

## 중간처리
괜찮은 결과를 얻으면 샘플링 단계를 약 32로 설정하고 원하는 것에 따라 6~30개의 이미지를 생성합니다. 
나는 보통 이것으로 좋은 결과(또는 하나 이상)를 얻습니다.



