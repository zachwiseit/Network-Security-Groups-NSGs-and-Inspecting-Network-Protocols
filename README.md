<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

1
<p>
<p>
<img <img width="1440" alt="ACN_1" src="https://github.com/user-attachments/assets/b16b0dad-c9ce-4f61-ac91-776b0748cd22" />
</p>
<p>
2
<p>
<img <img width="1440" alt="ACN_2" src="https://github.com/user-attachments/assets/7c4c3741-07ca-481f-86df-8f758318b919" />
</p>
<p>
3
<p>
<img <img width="1440" alt="ACN_3" src="https://github.com/user-attachments/assets/79cb82ce-6c74-4858-8d37-000d5c8e5690" />
</p>
<p>
4
<p>
<img <img width="1440" alt="ACN_4" src="https://github.com/user-attachments/assets/dafa6038-85f8-46a4-83c5-b6e7536b3ffb" />
</p>
<p>
5
<p>
<img <img width="1440" alt="ACN_5" src="https://github.com/user-attachments/assets/dd13c7dd-343c-4b43-aad5-24a171710042" />
</p>
<p>
6
<p>
<img <img width="1440" alt="ACN_6" src="https://github.com/user-attachments/assets/b3e8d161-c43d-4fa7-b097-fd51b2aea2d2" />
</p>
<p>
7
<p>
<img <img width="1440" alt="ACN_7" src="https://github.com/user-attachments/assets/fe27f401-6ac3-492d-892b-44d286eabe9e" />
</p>
<p>
8
<p>
<img <img width="1440" alt="ACN_8" src="https://github.com/user-attachments/assets/0de6188c-7407-4c7b-81d1-d7342218a34f" />
</p>
<p>
9
<p>
<img <img width="1440" alt="ACN_9" src="https://github.com/user-attachments/assets/ec9055a6-dcb0-4b80-8cb3-c15ef631e1e9" />
</p>
<p>
10
<p>
<img <img width="1440" alt="ACN_10" src="https://github.com/user-attachments/assets/d3d22d5d-14f2-4a81-892e-986c7c5138a5" />
</p>
<p>
11
<p>
<img <img width="1440" alt="ACN_11" src="https://github.com/user-attachments/assets/69b9be87-5df1-4cc8-baa9-dc27c4b7ef71" />
</p>
<p>
12
<p>
<img <img width="1440" alt="ACN_12" src="https://github.com/user-attachments/assets/2b5854b3-0f0b-4fc9-8321-e4010fbe85e8" />
</p>
<p>
13
<p>
<img <img width="1440" alt="ACN_13" src="https://github.com/user-attachments/assets/279242cb-cda4-47cf-a169-6e261d14e4dd" />
</p>
<p>
14
<p>
<img <img width="1440" alt="ACN_14" src="https://github.com/user-attachments/assets/78e40ba3-9aa7-4e70-808f-63b5c04cf1db" />
</p>
<p>
15
<p>
<img <img width="1440" alt="ACN_15" src="https://github.com/user-attachments/assets/b854355e-08b0-4f86-8d10-9a92bd000bcf" />
</p>
<p>
16
<p>
<img <img width="1440" alt="ACN_16" src="https://github.com/user-attachments/assets/e26dfb86-f0a7-4249-a977-462205c4f271" />
</p>
<p>
17
<p>
<img <img width="1440" alt="ACN_17" src="https://github.com/user-attachments/assets/286a0b99-0962-4ccb-825e-11861f543773" />
</p>
<p>
18
<p>
<img <img width="1440" alt="ACN_18" src="https://github.com/user-attachments/assets/eaca95d7-cabf-4268-811b-f385ccd2093b" />
</p>
<p>
19
<p>
<img <img width="1440" alt="ACN_19" src="https://github.com/user-attachments/assets/e9799a86-ab30-46a9-8731-77d06423d391" />
</p>
<p>
20
<p>
<img <img width="1440" alt="ACN_20" src="https://github.com/user-attachments/assets/c6774ed4-f42a-4507-a9f2-a5faa16eac45" />
</p>
<p>
21
<p>
<img <img width="1440" alt="ACN_21" src="https://github.com/user-attachments/assets/889be5af-0ad8-44b4-a7dd-07e24203af6b" />
</p>
<p>
22
<p>
<img <img width="1440" alt="ACN_22" src="https://github.com/user-attachments/assets/8f797673-3183-40b0-835c-756a5fa1b7ad" />
</p>
<p>
23
<p>
<img <img width="1440" alt="ACN_23" src="https://github.com/user-attachments/assets/6b4f66ec-1beb-4446-8544-cc3b5b90ba30" />
</p>
<p>
24
<p>
<img <img width="1440" alt="ACN_24" src="https://github.com/user-attachments/assets/4f735588-4b51-4a0a-a57a-620480583e31" />
</p>
<p>
25
<p>
<img <img width="1440" alt="ACN_25" src="https://github.com/user-attachments/assets/12610ff2-1adb-4223-8732-0351f0f6125a" />
</p>
<p>
26
<p>
<img <img width="1440" alt="ACN_26" src="https://github.com/user-attachments/assets/1dd204b8-e5fe-4c1c-9eb9-bb7ee24c29fe" />
</p>
<p>
27
<p>
<img <img width="1440" alt="ACN_27" src="https://github.com/user-attachments/assets/df3cb7cd-a25d-44ec-9095-42c725830b9c" />
</p>
<p>
28
<p>
<img <img width="1440" alt="ACN_28" src="https://github.com/user-attachments/assets/16aefb9d-b46b-4632-bdb4-eaf93cff3eb9" />
</p>
<p>
29
<p>
<img <img width="1440" alt="ACN_29" src="https://github.com/user-attachments/assets/d81cbe52-266e-46aa-86c4-0bc7477da193" />
</p>
<p>
30
<p>
<img <img width="1440" alt="ACN_30" src="https://github.com/user-attachments/assets/de766627-d11f-487f-bae1-08113e3a552c" />
</p>
<p>
31
<p>
<img <img width="1440" alt="ACN_31" src="https://github.com/user-attachments/assets/213491e1-cdd7-4f4c-9215-332195f27cb8" />
</p>
<p>
32
<p>
<img <img width="1440" alt="ACN_32" src="https://github.com/user-attachments/assets/cf78de25-1109-4de2-96cd-4762aafae966" />
</p>
<p>
33
<p>
<img <img width="1440" alt="ACN_33" src="https://github.com/user-attachments/assets/1b793641-22e6-4ce3-a69f-ee72ce278134" />
</p>
<p>
34
<p>
<img <img width="1440" alt="ACN_34" src="https://github.com/user-attachments/assets/f34995c7-b206-42a8-b91f-3645cab738b7" />
</p>
<p>
35
<p>
<img <img width="1440" alt="ACN_35" src="https://github.com/user-attachments/assets/3cbdd19f-5017-4f60-b816-e75163be1eca" />
</p>
<p>
36
<p>
<img <img width="1440" alt="ACN_36" src="https://github.com/user-attachments/assets/d2526ed3-5ac2-4199-9c38-b6a9b2c9c5ec" />
</p>
<p>
37
<p>
<img <img width="1440" alt="ACN_37" src="https://github.com/user-attachments/assets/a4cef65a-4820-409c-b67c-330138a62c33" />
</p>
<p>
38
<p>
<img <img width="1440" alt="ACN_38" src="https://github.com/user-attachments/assets/a0db48ff-0f61-4a3e-bc67-c9e0c6ed5fcd" />
</p>
<p>
39
<p>
<img <img width="1440" alt="ACN_39" src="https://github.com/user-attachments/assets/714c4afc-d546-40bf-82a6-c4415ff81e7f" />
</p>
<p>
40
<p>
<img <img width="1440" alt="ACN_40" src="https://github.com/user-attachments/assets/bacec360-b0ea-44d2-b5ea-4018c5462e12" />
</p>
<p>
41
<p>
<img <img width="1440" alt="ACN_41" src="https://github.com/user-attachments/assets/e6cfbebb-69f0-4d80-9721-7483ea1d524d" />
</p>
<p>
42
<p>
<img <img width="1440" alt="ACN_42" src="https://github.com/user-attachments/assets/74f3c9ab-6515-4004-8c22-91cb9a44c51a" />
</p>
<p>
43
<p>
<img <img width="1440" alt="ACN_43" src="https://github.com/user-attachments/assets/c8b9fef7-684d-4d6b-abfa-0e98e63e1c22" />
</p>
<p>
44
<p>
<img <img width="1440" alt="ACN_44" src="https://github.com/user-attachments/assets/786aedbc-b8ba-4c55-8381-23e3875314f8" />
</p>
<p>
45
<p>
<img <img width="1440" alt="ACN_45" src="https://github.com/user-attachments/assets/4f1b002f-7b29-4a99-ac7f-0208815c2cea" />
</p>
<p>
46
<p>
<img <img width="1440" alt="ACN_46" src="https://github.com/user-attachments/assets/add6ed94-3996-44b4-84a6-b91afd8999f2" />
</p>
<p>
47
<p>
<img <img width="1440" alt="ACN_47" src="https://github.com/user-attachments/assets/b1c45af4-ced6-4eb1-a704-ab5547a2971e" />
</p>
<p>
48
<p>
<img <img width="1440" alt="ACN_48" src="https://github.com/user-attachments/assets/3550a500-84e1-41ba-b504-d2c19790486c" />
</p>
<p>
49
<p>
<img <img width="1440" alt="ACN_49" src="https://github.com/user-attachments/assets/d64bb8d4-fde8-4088-9e5b-d37789877b19" />
</p>
<p>
50
<p>
<img <img width="1440" alt="ACN_50" src="https://github.com/user-attachments/assets/d974ec18-861e-453c-b505-343982a899e0" />
</p>
<p>
51
<p>
<img <img width="1440" alt="ACN_51" src="https://github.com/user-attachments/assets/80697e72-29ae-43fb-aed1-cd2b1358525a" />
</p>
<p>
52
<p>
<img <img width="1440" alt="ACN_52" src="https://github.com/user-attachments/assets/f1189ef0-29ba-4783-abca-0d6399198cd6" />
</p>
<p>
53
<p>
<img <img width="1440" alt="ACN_53" src="https://github.com/user-attachments/assets/70fff573-4e24-472a-82b3-bf7d1f34fda9" />
</p>
<p>
54
<p>
<img <img width="1440" alt="ACN_54" src="https://github.com/user-attachments/assets/e2cc8519-9ec6-44fc-a288-20df9ba0c58c" />
</p>
<p>
55
<p>
<img <img width="1440" alt="ACN_55" src="https://github.com/user-attachments/assets/1f344563-a8d9-4e8c-8e76-7d15f5d7009a" />
</p>
<p>
56
<p>
<img <img width="1440" alt="ACN_56" src="https://github.com/user-attachments/assets/38e6f56a-dd25-4558-bccb-9b0a674b9a5f" />
</p>
<p>
57
<p>
<img <img width="1440" alt="ACN_57" src="https://github.com/user-attachments/assets/b9c2f8d4-9f07-48b0-943c-f54b0744b8e6" />
</p>
<p>
58
<p>
<img <img width="1440" alt="ACN_58" src="https://github.com/user-attachments/assets/7ce8ead3-8855-4d0e-97f6-5964ea29b285" />
</p>
<p>
59
<p>
<img <img width="1440" alt="ACN_59" src="https://github.com/user-attachments/assets/5d76b691-7e6f-4953-b4e5-8b52fb044b49" />
</p>
<p>
60
<p>
<img <img width="1440" alt="ACN_60" src="https://github.com/user-attachments/assets/5378c3b9-829f-4718-91b6-30f46ba0415d" />
</p>
<p>
61
<p>
<img <img width="1440" alt="ACN_61" src="https://github.com/user-attachments/assets/808b3524-5795-49b4-a153-57ffe4df1e69" />
</p>
<p>
62
<p>
<img <img width="1440" alt="ACN_62" src="https://github.com/user-attachments/assets/5d8b6cff-9fc0-43c8-be74-6432ffa6696a" />
</p>
<p>
63
<p>
<img <img width="1440" alt="ACN_63" src="https://github.com/user-attachments/assets/80ac5862-a61d-47c2-90f0-4bd2c0e662a6" />
</p>
<p>
64
<p>
<img <img width="1440" alt="ACN_64" src="https://github.com/user-attachments/assets/2ceaeae0-41ff-421a-b91b-9347ef06a8dc" />
</p>
<p>
65
<p>
<img <img width="1440" alt="ACN_65" src="https://github.com/user-attachments/assets/c5add192-3d50-47b1-b1b2-4dac2eb16f75" />
</p>
<p>
66
<p>
<img <img width="1440" alt="ACN_66" src="https://github.com/user-attachments/assets/3622f977-d579-4b5b-8e6b-3235b9cabc20" />
</p>
<p>
67
<p>
<img <img width="1440" alt="ACN_67" src="https://github.com/user-attachments/assets/0bba4378-3bb3-4470-8f7e-c1bee73be62a" />
</p>
<p>
68
<p>
<img <img width="1440" alt="ACN_68" src="https://github.com/user-attachments/assets/c1a3a627-591a-4cbf-a407-0aaf1bf48038" />
</p>
<p>
69
<p>
<img <img width="1440" alt="ACN_69" src="https://github.com/user-attachments/assets/9dab7b31-b72b-46b2-8879-8584d6cbb27f" />
</p>
<p>
70
<p>
<img <img width="1440" alt="ACN_70" src="https://github.com/user-attachments/assets/e26ebbd6-8064-439f-a2a6-dbffbc5a0dcf" />
</p>
<p>
71
<p>
<img <img width="1440" alt="ACN_71" src="https://github.com/user-attachments/assets/805f82de-d391-433a-b345-68ef5f6d1115" />
</p>
<p>
72
<p>
<img <img width="1440" alt="ACN_72" src="https://github.com/user-attachments/assets/9e96c173-38b7-43d8-bee5-4a87a30143b1" />
</p>
<p>
73
<p>
<img <img width="1440" alt="ACN_73" src="https://github.com/user-attachments/assets/646c5268-ca60-4f79-bc0e-103b1230331b" />
</p>
<p>
74
<p>
<img <img width="1440" alt="ACN_74" src="https://github.com/user-attachments/assets/7bafff74-e75a-4956-b0fe-f454f2198e25" />
</p>
<p>
75
<p>
<img <img width="1440" alt="ACN_75" src="https://github.com/user-attachments/assets/8c71d513-935b-4693-a072-173237710433" />
</p>
<p>
76
<p>
<img <img width="1440" alt="ACN_76" src="https://github.com/user-attachments/assets/e26b373f-7ed7-485a-a5fa-5d856a524b29" />
</p>
<p>
77
<p>
<img <img width="1440" alt="ACN_77" src="https://github.com/user-attachments/assets/276db2ed-5e74-41a0-99e6-218c3c0bd05e" />
</p>
<p>
78
<p>
<img <img width="1440" alt="ACN_78" src="https://github.com/user-attachments/assets/4d020138-eefd-411c-b45e-8867d8b7ddc7" />
</p>
<p>
79
<p>
<img <img width="1440" alt="ACN_79" src="https://github.com/user-attachments/assets/3a2f43b0-6f2e-453d-a69c-e5f53c174e2b" />
</p>
<p>
80
<p>
<img <img width="1440" alt="ACN_80" src="https://github.com/user-attachments/assets/261e4b7f-117f-486f-a2e9-461f0ef133dd" />
</p>
<p>
81
<p>
<img <img width="1440" alt="ACN_81" src="https://github.com/user-attachments/assets/6a57f506-df4e-436f-8c69-e8cc25fbb974" />
</p>
<p>
82
<p>
<img <img width="1440" alt="ACN_82" src="https://github.com/user-attachments/assets/224e0e1f-2f38-4d4b-9be7-1bd7e41afede" />
</p>
<p>
83
<p>
<img <img width="1440" alt="ACN_83" src="https://github.com/user-attachments/assets/1959b108-e451-4cf3-a0d1-7ff5d493fd89" />
</p>
<p>
84
<p>
<img <img width="1440" alt="ACN_84" src="https://github.com/user-attachments/assets/8be852ba-41a4-4a52-afe4-9469ddd0c773" />
</p>
<p>
85
<p>
<img <img width="1440" alt="ACN_85" src="https://github.com/user-attachments/assets/2559f588-3dd7-4995-913e-787f708b0f13" />
</p>
<p>
86
<p>
<img <img width="1440" alt="ACN_86" src="https://github.com/user-attachments/assets/c2cbbe47-02f4-4dc9-b7c2-dc353a36cd5a" />
</p>
<p>
87
<p>
<img <img width="1440" alt="ACN_87" src="https://github.com/user-attachments/assets/16040530-ceda-4a5b-90e5-d2ca470ca31b" />
</p>
<p>
88
<p>
<img <img width="1440" alt="ACN_88" src="https://github.com/user-attachments/assets/bc852034-48d2-4b59-aad6-e43f17288ee8" />
</p>
<p>
89
<p>
<img <img width="1440" alt="ACN_89" src="https://github.com/user-attachments/assets/e15dac2f-75c3-47f3-a49a-a7afbab940f7" />
</p>
<p>
90
<p>
<img <img width="1440" alt="ACN_90" src="https://github.com/user-attachments/assets/4b321fd6-f444-43f3-897a-d7d8687196ea" />
</p>
<p>
91
<p>
<img <img width="1440" alt="ACN_91" src="https://github.com/user-attachments/assets/39cbb2fa-0a73-4d23-9454-8d95ac0184b2" />
</p>
<p>
92
<p>
<img <img width="1440" alt="ACN_92" src="https://github.com/user-attachments/assets/689f0312-6b66-4a3a-a2e4-d23bc6d8b89d" />
</p>
<p>
93
<p>
<img <img width="1440" alt="ACN_93" src="https://github.com/user-attachments/assets/95ea1f22-d1ae-423b-a762-9d808dfb001d" />
</p>
<p>
94
<p>
<img <img width="1440" alt="ACN_94" src="https://github.com/user-attachments/assets/407e3736-f043-4ca7-b1bc-c17484b07a59" />
</p>
<p>
95
<p>
<img <img width="1440" alt="ACN_95" src="https://github.com/user-attachments/assets/5b858b58-d471-4fbd-9519-6cc569502ef7" />
</p>
<p>
96
<p>
<img <img width="1440" alt="ACN_96" src="https://github.com/user-attachments/assets/e8484d67-bb66-414b-94db-37019c013bee" />
</p>
<p>
97
<p>
<img <img width="1440" alt="ACN_97" src="https://github.com/user-attachments/assets/ff94b629-e189-40fc-af45-931b2ad4879b" />
</p>
<p>
98
<p>
<img <img width="1440" alt="ACN_98" src="https://github.com/user-attachments/assets/6350a7ce-06b9-4fae-bf52-1211d3b75141" />
</p>
<p>
99
<p>
<img <img width="1440" alt="ACN_99" src="https://github.com/user-attachments/assets/cb76dbad-cf24-4f1e-b03c-20967ddf577a" />
</p>
<p>
100
<p>
<img </p>
<p>
