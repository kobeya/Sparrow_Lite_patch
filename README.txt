CORE change list:

	①ADD two 10.1_inch_LCD :

		1.KD101N89_LCD (form K&D company)
		dsi-panel-kd101n89-800p-video.dtsi
		apq8053-lite-lenovo-v1.4.dtsi
		apq8053-lite-lenovo-v1.4.dts

		2.JD9365_LCD (form Starry company)
		dsi-panel-jd9365-800p-video.dtsi
		apq8053-lite-lenovo-v1.5.dtsi
		apq8053-lite-lenovo-v1.5.dts

	and change in kernel:
		Makefile
		msm8953-mdss-panel.dtsi

LCD Compatibility:sparrow/hardware/bsp/kernel/qcom/qcom-msm8x53-v3.18/drivers/video/msm/mdss/mdss_dsi.c +2973

	KD101N89_LCD:gpio140_value=0
		     gpio141_value=1
	
	JD9365_LCD:  gpio140_value=1
		     gpio141_value=1

	

