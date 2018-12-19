CORE change list:
	                       Update deadline:2018/12/19
	1.need CDT>=1.3 to bring up starry 10.1 LCD
	2.https://github.com/kobeya/Sparrow_Lite_kernel_CDT

	①ADD two 10.1_inch_LCD :

		1.KD101N89_LCD (form K&D company)
		dsi-panel-kd101n89-800p-video.dtsi
		apq8053-lite-lenovo-v1.5.dtsi
		apq8053-lite-lenovo-v1.5.dts
		(WARNING:
			At present, the code uploaded to GitHub can only make starry_LCD work.
			But in the code, there are also initialization codes and drivers for K&D_LCD just let qcom know that the LCD code actually exists.
		)
		2.STARRY_LCD (form Starry company)  
		dsi-panel-starry-800p-video.dtsi
		apq8053-lite-lenovo-v1.4.dtsi

	and change in kernel:
		Makefile
		msm8953-mdss-panel.dtsi

LCD Compatibility:sparrow/hardware/bsp/kernel/qcom/qcom-msm8x53-v3.18/drivers/video/msm/mdss/mdss_dsi.c +2973

	KD101N89_LCD:gpio140_value=0
		     gpio141_value=0
	
	JD9365_LCD:  gpio140_value=0
		     gpio141_value=1

	②ADD 4E8_camera （IC：s5k4e8）
		1.bring up camera
		2.camera is tuning by Samsung company right now	

