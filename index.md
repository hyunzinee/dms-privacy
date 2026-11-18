---
layout: default
title: DMS 졸음감지 개인정보처리방침
---

# DMS 졸음감지 개인정보처리방침

시행일: 2026년 11월 19일

DMS 졸음감지(이하 "앱", 패키지명 `io.github.hyunzinee.dms`)는 운전자의 졸음을 감지하기 위해 스마트폰 전면 카메라를 사용합니다. 이 방침은 앱이 어떤 정보를 어떻게 다루는지 설명합니다.

## 1. 요약
- 앱은 **어떤 개인정보도 수집하거나 외부로 전송하지 않습니다.**
- 카메라 영상은 **기기 안에서만 실시간으로 분석**되며 저장되지 않습니다.
- 위치(GPS)는 **정차 여부 판단에만 기기 안에서 사용**되며 저장·전송되지 않습니다.
- 앱에는 **인터넷 권한이 없어** 기술적으로 데이터를 외부로 보낼 수 없습니다.
- 광고, 분석(Analytics), 계정 기능이 없습니다.

## 2. 카메라
- 목적: 눈 개방도, 입 모양, 머리 각도를 측정해 졸음 여부를 판단합니다.
- 처리 방식: 카메라 프레임은 Google MediaPipe Face Landmarker 모델로 **기기 내부에서** 분석되며, 분석 직후 메모리에서 폐기됩니다. 사진이나 영상은 저장·녹화·전송되지 않습니다.
- 백그라운드: 사용자가 감시를 시작하면 다른 앱을 쓰거나 화면이 꺼져도 감시가 계속되며, 이때 상단 알림("졸음 감시 중")이 항상 표시됩니다. 알림 또는 앱의 "감시 종료"로 언제든 중지할 수 있습니다.

## 3. 위치 (선택)
- 목적: "정차 중 경보 중지" 기능을 켠 경우, GPS 속도로 차량이 멈춰 있는지 판단해 정차 중에는 경보를 울리지 않습니다.
- 처리 방식: 위치 좌표와 속도는 기기 안에서 "정차/주행" 판단에만 쓰이고 즉시 폐기됩니다. 위치 기록을 저장하거나 외부로 전송하지 않습니다.
- 감시 중일 때만 사용하며(상단 알림 표시), 백그라운드 위치 권한("항상 허용")은 요청하지 않습니다.
- 위치 권한을 거부하거나 설정에서 기능을 끄면 GPS를 사용하지 않으며, 경보는 항상 정상적으로 울립니다.

## 4. 기기에 저장되는 정보
앱 설정만 기기 내부 저장소에 보관됩니다.
- 눈 감음 임계값, 경보 지연 시간, 카메라 화면 표시 여부
- 설정 화면의 감지 기준(고개 숙임 각도, 하품 기준 등)과 GPS 기능 사용 여부
- 보정 결과(평소 눈 개방도 기준값, 정면 머리 각도 숫자)

이 값들은 얼굴 이미지가 아닌 숫자이며, 기기 밖으로 나가지 않습니다. 앱을 삭제하면 함께 삭제됩니다. 기기 백업에도 포함되지 않습니다.

## 5. 권한
| 권한 | 용도 |
|---|---|
| 카메라 | 운전자 얼굴 분석 (기기 내부) |
| 알림 | 감시 중 표시, 졸음 경보 알림 |
| 위치 (선택) | 정차 여부 판단 (기기 내부, 저장·전송 없음) |
| 포그라운드 서비스(카메라·위치) | 다른 앱 사용 중·화면 꺼짐 상태에서도 감시 유지 |
| 화면 꺼짐 방지(Wake lock) | 화면이 꺼져도 분석이 멈추지 않도록 유지 |
| 진동 | 졸음 경보 |

## 6. 제3자 제공
수집하는 정보가 없으므로 제3자에게 제공하는 정보도 없습니다. 앱에 포함된 MediaPipe 라이브러리의 사용 통계 기능은 인터넷 권한이 없어 동작하지 않습니다.

## 7. 아동
앱은 운전자를 위한 앱이며 만 18세 미만을 대상으로 하지 않습니다.

## 8. 안전 고지
앱은 운전 보조 도구이며 졸음운전을 완전히 예방하지 못합니다. 졸음이 느껴지면 반드시 안전한 곳에서 휴식하세요. 운전 중에는 앱을 조작하지 마세요.

## 9. 변경
방침이 바뀌면 이 페이지에 게시하고 시행일을 갱신합니다.

## 10. 문의
hyunzinee@gmail.com

---

# DMS Drowsiness Monitor Privacy Policy

Effective: November 19, 2026

DMS Drowsiness Monitor ("the app", package `io.github.hyunzinee.dms`) uses the phone's front camera to detect driver drowsiness.

- The app **does not collect or transmit any personal data**.
- Camera frames are **analyzed on the device in real time** with Google MediaPipe Face Landmarker and discarded immediately. No photos or videos are stored, recorded, or sent.
- Location (optional): when "pause alarms while stopped" is on, GPS speed is used on the device only to decide whether the vehicle is stopped, then discarded. Location is never stored or sent, is used only while monitoring (ongoing notification shown), and background ("allow all the time") location is not requested. Without the permission, alarms always sound.
- The app has **no Internet permission**, so it cannot send data off the device. There are no ads, analytics, or accounts.
- Only settings (alert threshold, alert delay, preview on/off) and calibration numbers (baseline eye openness, forward head angle) are stored locally. They are not images, never leave the device, are excluded from backups, and are deleted when the app is uninstalled.
- Permissions: camera (on-device face analysis), location (optional, on-device stop detection), notifications (monitoring status and alarms), camera/location foreground service and wake lock (keep monitoring in the background / with the screen off while the ongoing notification is shown), vibration (alarm).
- The MediaPipe library's usage-statistics feature cannot operate because the app has no Internet permission.
- The app is intended for drivers and is not directed at children under 18.
- The app is a driving aid and cannot fully prevent drowsy driving. If you feel drowsy, stop in a safe place and rest. Do not operate the app while driving.
- Contact: hyunzinee@gmail.com
