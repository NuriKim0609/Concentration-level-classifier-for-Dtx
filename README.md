# Concentration-level-classifier-for-Dtx
# Dataset
Zyma I, Tukaev S, Seleznov I, Kiyono K, Popov A, Chernykh M, Shpenkov O. Electroencephalograms during Mental Arithmetic Task Performance. Data. 2019; 4(1):14. https://doi.org/10.3390/data4010014
# Data Acquisition (EEG Signal Recording)
The dataset was collected using the Neurocom EEG 23-channel system (XAI-MEDICA, Ukraine), with EEG signals recorded in a monopolar configuration. Electrodes were placed on the scalp according to the international 10–20 system. To remove noise, a high-pass filter with a cut-off frequency of 30 Hz and a 50 Hz notch filter were applied. The high-pass filter allowed signals with frequencies higher than the cut-off value to pass, while the notch filter—a narrow-band filter—removed only signals around 50 Hz without affecting the rest of the signal.
The experiment involved 36 participants (27 female, 9 male). Each participant underwent EEG recording in two separate conditions: before and during the execution of a mental arithmetic task. The task involved sequential subtraction of 42 from 3141 (i.e., 3141 − 42, repeatedly).
EEG Recording System:
Data were collected using the Neurocom EEG 23-channel system (XAI-MEDICA, Ukraine), with EEG signals recorded in a monopolar configuration.

Electrode Placement:
Electrodes were positioned according to the international 10–20 system.

Preprocessing:
To eliminate noise:

A high-pass filter with a cut-off frequency of 30 Hz was applied to retain signals above this threshold.

A 50 Hz notch filter was used to remove power-line interference without affecting other frequency bands.

Participants:
EEG data were recorded from 36 participants:

27 females, 9 males

Experimental Procedure:

Each participant completed EEG sessions in two separate states:

Pre-task resting state

During a mental arithmetic task

The task required participants to repeatedly subtract 42 from 3141 (e.g., 3141 − 42, then −42 again, etc.)


본 데이터 세트는 Neurocom EEG 23채널 시스템(우크라이나, XAI-MEDICA)을 사용하여 뇌파를 단극 방식(monopolar)으로 기록하였다. 전극은 국제 10/20 시스템에 따라 두피에 배치되었으며, 30 Hz의 차단 주파수(Cut-off Frequency)와 50Hz 노치 필터 (50Hz Notch Filter)를 적용한 고역통과 필터(High-pass filter)를 통해 노이즈를 제거하였다. 차단 주파수를 지정한 고역통과 필터는 지정 주파수 값보다 큰 주파수를 가지는 신호들만 포함시키는 필터인 반면 노치 필터는 협대역 필터로 특정 주파수와 그 근처만 제거하며, 나머지 신호에는 영향을 주지 않는다. 실험은 총 36명의 피험자(여성:27명, 남성:9명)를 대상으로 진행되었다. 각 피험자는 연산 과제 수행 전과 수행 중의 두 가지 상태에 대해 개별적으로 뇌파 측정을 진행하였으며, 3141에서 42를 차례로 빼라는 연산 과제를 부여받았다.

# Dataset Construction

EEG 데이터 파일은 EDF(European Data Format) 형식으로 제공되며, 각 피험자의 연산 과제 이전("_1")과 수행 중("_2" )의 EEG 기록은 분리되어 각 피험자 별 두 개의 파일이 제공된다. 또한 참가자들의 연산 과제 수행 성과를 기준으로 우수그룹("G" 그룹: 24명, 분당 평균 연산 횟수 = 21, 표준편차 = 7.4) 과 미흡그룹("B" 그룹: 12명, 4분당 평균 연산 횟수 = 7, 표준편차 = 3.6)으로 나누어져 있다. 따라서 향후 DTx 사용자들의 EEG 분석 시 휴식/집중 상태 분류뿐만 아니라 문제 풀이 능력을 파악하는 데에도 활용할 수 있어더욱 정확한 분류기 생성 및 개인 맞춤형 DTx 개발을 위한 자료로 활용될 수 있다. 아래의 그림 X은 두번째 피험자의 연산과제 수행 전과 수행 중의 뇌파로 23개 채널에 대한 60초간의 측정 기록을 나타내고 있다. 

