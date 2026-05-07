# Character Power Curve

`character-power-curve`는 한국 웹소설 주인공의 성장곡선, 능력 개방 타이밍, 위기 강도, 보상구조, 지위 상승, rival scaling을 설계하고 진단하는 Codex 스킬입니다.

헌터물, 탑등반, 회귀, 빙의, 시스템, 성좌, 아카데미, 무협, 판타지, 로판/악역영애, 재벌/경영, 연예계, 스포츠, 요리, 제작, 생존형 엑스트라물처럼 “주인공이 강해져야 하지만 긴장감은 죽으면 안 되는” 장기 연재형 서사에 맞춰져 있습니다.

## What This Skill Does

- 주인공 타입을 장르별로 세분화해 판정합니다.
- 먼치킨, 성장형, 회귀자, 빙의자, 천재형, 노력형, 악역영애, 엑스트라 생존형 등에 맞는 성장곡선을 설계합니다.
- 주인공이 세계 안에서 어떤 위치로 보이는지, 즉 위치강조를 잡습니다.
- 능력, 지위, 자원, 부담을 나눠 보상구조를 설계합니다.
- 주인공이 강해진 뒤에도 긴장감이 유지되도록 위기 강도와 다음 천장을 조절합니다.
- 100종 이상 주인공 타입 카탈로그를 참조해 후보 타입과 장단점을 제안합니다.
- 단일 타입이 애매한 경우 `기원 × 능력 × 세계 내 위치 × 결핍` 매트릭스로 혼합형 주인공을 설계합니다.

## Files

```text
character-power-curve/
├─ SKILL.md
├─ README.md
├─ LICENSE.txt
├─ agents/
│  └─ openai.yaml
└─ references/
   ├─ advanced-playbook.md
   ├─ archetype-combination-matrix.md
   ├─ diagnostic-playbooks.md
   ├─ growth-curve-patterns.md
   ├─ output-templates.md
   └─ protagonist-type-catalog.md
```

## Install With Codex

Codex의 `$skill-installer`를 사용할 수 있다면 저장소 루트를 스킬 폴더로 지정해 설치할 수 있습니다.

```text
$skill-installer install from repo ansrhkddns-web/character-power-curve with path . and name character-power-curve
```

설치 후 Codex를 재시작해야 새 스킬이 인식됩니다.

`skill-installer` helper script를 직접 실행하는 경우에는 아래 형식을 사용합니다.

```text
python scripts/install-skill-from-github.py --repo ansrhkddns-web/character-power-curve --path . --name character-power-curve
```

## Sharing Link

저장소 루트에 `SKILL.md`가 있으므로 공유용 기본 링크는 아래 주소입니다.

```text
https://github.com/ansrhkddns-web/character-power-curve
```

현재 `skill-installer`는 저장소 루트 URL만으로는 설치 경로 이름을 안정적으로 추론하지 않으므로, 설치 안내에는 `repo + path . + name character-power-curve` 형식을 함께 쓰는 것이 가장 명확합니다.

```text
repo: ansrhkddns-web/character-power-curve
path: .
name: character-power-curve
```

만약 나중에 스킬을 저장소 하위 폴더로 옮긴다면, 공유 링크도 해당 폴더까지 포함해야 합니다.

## Example Prompts

```text
Use $character-power-curve to design a hunter regression protagonist's growth curve.
```

```text
$character-power-curve로 악역영애 생존형 주인공의 보상구조와 위기 강도를 설계해줘.
```

```text
재벌물 빙의자 주인공이 중반부부터 너무 쉽게 이기는 문제가 있어. 성장곡선과 다음 천장을 진단해줘.
```

```text
아카데미 먼치킨 주인공인데 긴장감이 죽지 않게 위치강조와 rival scaling을 잡아줘.
```

```text
헌터물 회귀자+제작자+재벌형을 섞은 주인공 타입을 만들고 25화까지 성장곡선을 설계해줘.
```

```text
회귀자 주인공이 너무 쉽게 이겨서 중반부 긴장감이 죽었어. 최소 수정으로 살려줘.
```

## Recommended Output

이 스킬은 기본적으로 다음 항목을 포함한 “진단+설계표”를 반환하도록 설계되어 있습니다.

- 주인공 타입 진단
- 성장곡선 스타일
- 위치강조
- 보상구조
- 위기 강도 조절
- 다음 5-15화 적용안
- 혼합형 주인공일 경우 기원, 능력, 위치, 결핍 조합표

## License And Attribution

이 스킬은 MIT License로 배포됩니다. 자세한 내용은 `LICENSE.txt`를 확인하세요.

스킬을 공유하거나 수정 배포할 때는 원 저장소 링크를 함께 표기하는 것을 권장합니다.
