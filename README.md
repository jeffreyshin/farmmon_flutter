# farmmon_flutter

딸기 탄저병, 잿빛곰팡이병 발생 모니터링을 위한 안드로이드앱
- 충남 논산딸기연구소의 모델을 사용함

1. Layout: 품목을 좌측메뉴에 놓고 품목을 선택하면 우측창에 병해충별 위험도를 나타냄
2. 좌측창의 아이콘 품목아이콘으로 수정할 것
3. 우측창에는 fl_chart를 이용하여 날짜별 막대그래프로 위험도 표시
4. HTTP API post SNFD로 확인 완료. file이 잘 안되서 json전송방식으로 바꾸기로 했음
5. 일단, iot포털데이터를 받아서 그래프 업데이트만 구현함
7. 데이터 가져온후 그래프 갱신을 위해 appstate 방식 검토필요


Future<String> uploadImage(File file) async { String fileName = file.path.split('/').last; FormData formData = FormData.fromMap({ "file": await MultipartFile.fromFile(file.path, filename:fileName), }); response = await dio.post("/info", data: formData); return response.data['id']; }

var response = await dio.post(
'주소',
data: FormData.fromMap({
'content':content,
'file':file,
})
);

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.



![usem](https://github.com/jeffreyshin/farmmon_flutter/assets/6800894/e174988b-7b9e-4fb5-bdba-68bac337ae7f)

             
.                  
                  
                  
                
