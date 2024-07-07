# Smartfox data extraction

Some random notes about findings in the [Smartfox](https://smartfox.at) web API, and how to integrate it into [Home Assistant](https://www.home-assistant.io).

## Reading values

We can read some live data from the Smartfox on http://smartfox/values.xml:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<values>
	<value id="hidWebinterfaceVersion">a53ca932e4ab608af52a</value>
	<value id="macAddress">....</value>
	<value id="ipAddress">192.168.000.232</value>
	<value id="version">EM2  00.01.08.07</value>
	<value id="toGridValue">0.51 kW</value>
	<value id="lang">de</value>
	<value id="dateValue">2024-07-07</value>
	<value id="timeValue">13:33:32 Uhr</value>
	<value id="hidApiKey">....</value>
	<value id="socketIP">093.189.025.182</value>
	<value id="socketPort">5001</value>
	<value id="hidAoutMode">0</value>
	<value id="analogOutDescription">Analog</value>
	<value id="analogOutPercent">0%</value>
	<value id="analogOutPower">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="analogOutTemp">0.0 &#176;C</value>
	<value id="hidAoutActivated">0</value>
	<value id="hidAoutStatus">11</value>
	<value id="hidAoutName">Analog</value>
	<value id="hidCcType1">0</value>
	<value id="hidCcMode1">0</value>
	<value id="hidCcSt1">255</value>
	<value id="hidCcType2">0</value>
	<value id="hidCcMode2">0</value>
	<value id="hidCcSt2">255</value>
	<value id="hidCcType3">0</value>
	<value id="hidCcMode3">0</value>
	<value id="hidCcSt3">255</value>
	<value id="hidCcType4">0</value>
	<value id="hidCcMode4">0</value>
	<value id="hidCcSt4">255</value>
	<value id="hidCcType5">0</value>
	<value id="hidCcMode5">0</value>
	<value id="hidCcSt5">255</value>
	<value id="hidCcConnTimeout1">0</value>
	<value id="hidCcConnTimeout2">0</value>
	<value id="hidCcConnTimeout3">0</value>
	<value id="hidCcConnTimeout4">0</value>
	<value id="hidCcConnTimeout5">0</value>
	<value id="hidCc1Percent">100</value>
	<value id="hidCc2Percent">0</value>
	<value id="hidCc3Percent">0</value>
	<value id="hidCc4Percent">0</value>
	<value id="hidCc5Percent">0</value>
	<value id="hidCcRfid">["","","","",""]</value>
	<value id="hidCc1Username"></value>
	<value id="hidCc2Username"></value>
	<value id="hidCc3Username"></value>
	<value id="hidCc4Username"></value>
	<value id="hidCc5Username"></value>
	<value id="hidCc1Info">0</value>
	<value id="hidCc2Info">0</value>
	<value id="hidCc3Info">0</value>
	<value id="hidCc4Info">0</value>
	<value id="hidCc5Info">0</value>
	<value id="hidCc1Name">CC</value>
	<value id="hidCc2Name">CC</value>
	<value id="hidCc3Name">CC</value>
	<value id="hidCc4Name">CC</value>
	<value id="hidCc5Name">CC</value>
	<value id="hidCc1Phase">1</value>
	<value id="hidCc2Phase">1</value>
	<value id="hidCc3Phase">1</value>
	<value id="hidCc4Phase">1</value>
	<value id="hidCc5Phase">1</value>
	<value id="hidCc1TempTime">0</value>
	<value id="hidCc2TempTime">0</value>
	<value id="hidCc3TempTime">0</value>
	<value id="hidCc4TempTime">0</value>
	<value id="hidCc5TempTime">0</value>
	<value id="hidCc1Temperature">0</value>
	<value id="hidCc2Temperature">0</value>
	<value id="hidCc3Temperature">0</value>
	<value id="hidCc4Temperature">0</value>
	<value id="hidCc5Temperature">0</value>
	<value id="hidCc1VoS">0</value>
	<value id="hidCc2VoS">0</value>
	<value id="hidCc3VoS">0</value>
	<value id="hidCc4VoS">0</value>
	<value id="hidCc5VoS">0</value>
	<value id="hidCc1RemTimeSwitch">0</value>
	<value id="hidCc2RemTimeSwitch">0</value>
	<value id="hidCc3RemTimeSwitch">0</value>
	<value id="hidCc4RemTimeSwitch">0</value>
	<value id="hidCc5RemTimeSwitch">0</value>
	<value id="hidCcMplusMode">[0,0,0,0,0]</value>
	<value id="hidCcRemTimerEnergy">[71582.78,71582.78,71582.78,71582.78,71582.78]</value>
	<value id="hidCcRemTimerTime">[38400,0,45,0,0]</value>
	<value id="hidCcPhaseCurrent">[[0,0,0],[0,0,0],[0,0,0],[0,0,0],[0,0,0]]</value>
	<value id="hidCcControlCurrent">[0,0,0,0,0]</value>
	<value id="hidCcLimitInfo">[0,0,0,0,0]</value>
	<value id="hidCcProd">0</value>
	<value id="hidCc1EnergyDay">0.00</value>
	<value id="hidCc2EnergyDay">0.00</value>
	<value id="hidCc3EnergyDay">0.00</value>
	<value id="hidCc4EnergyDay">0.00</value>
	<value id="hidCc5EnergyDay">0.00</value>
	<value id="hidCc1CycleCounter">0</value>
	<value id="hidCc2CycleCounter">0</value>
	<value id="hidCc3CycleCounter">0</value>
	<value id="hidCc4CycleCounter">0</value>
	<value id="hidCc5CycleCounter">0</value>
	<value id="hidLic">0</value>
	<value id="detailsPowerValue">510 W</value>
	<value id="energyValue">13105.722 kWh</value>
	<value id="eApparentValue">3120 VAh</value>
	<value id="eDayValue">2495 Wh</value>
	<value id="eDayUsedValue">0 Wh</value>
	<value id="pUserValue">0 W</value>
	<value id="eToGridValue">20913.221 kWh</value>
	<value id="eUsedValue">0.000 kWh</value>
	<value id="eDayToGridValue">5239 Wh</value>
	<value id="relayStatusValue1">1</value>
	<value id="relayStatusValue2">0</value>
	<value id="relayStatusValue3">0</value>
	<value id="relayStatusValue4">0</value>
	<value id="relayRemTimeValue1">566 min</value>
	<value id="relayRemTimeValue2">0 min</value>
	<value id="relayRemTimeValue3">0 min</value>
	<value id="relayRemTimeValue4">65274 min</value>
	<value id="relayRunTimeValue1">34 min</value>
	<value id="relayRunTimeValue2">0 min</value>
	<value id="relayRunTimeValue3">0 min</value>
	<value id="relayRunTimeValue4">263 min</value>
	<value id="heatPumpPower">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="wpPowerValueIDM">0.00 kW</value>
	<value id="wpEnergyValueIDM">0.00 kWh</value>
	<value id="wpThermPowerValue">0.00 kW</value>
	<value id="wpTempBufferHotValue">0.0 &#176;C</value>
	<value id="wpTempWarmWaterValue1">0.0 &#176;C</value>
	<value id="wpThermEnergyValue">0.00 kWh</value>
	<value id="wpTempBufferColdValue">0.0 &#176;C</value>
	<value id="hidWpStatus">0</value>
	<value id="hidWpConnTimeout">0</value>
	<value id="hidBatteryConnTimeout1">0</value>
	<value id="hidBatteryConnTimeout2">0</value>
	<value id="hidBatteryConnTimeout3">0</value>
	<value id="voltageL1Value">236 V</value>
	<value id="voltageL2Value">239 V</value>
	<value id="voltageL3Value">237 V</value>
	<value id="ampereL1Value">2.74 A</value>
	<value id="ampereL2Value">1.82 A</value>
	<value id="ampereL3Value">2.38 A</value>
	<value id="powerL1Value">385 W</value>
	<value id="powerL2Value">-376 W</value>
	<value id="powerL3Value">501 W</value>
	<value id="wr1PowerValue">3.98 kW</value>
	<value id="wr2PowerValue">0.00 kW</value>
	<value id="wr3PowerValue">0.00 kW</value>
	<value id="wr4PowerValue">0.00 kW</value>
	<value id="wr5PowerValue">0.00 kW</value>
	<value id="wr1CustomerName">Plenticore</value>
	<value id="wr2CustomerName"></value>
	<value id="wr3CustomerName"></value>
	<value id="wr4CustomerName"></value>
	<value id="wr5CustomerName"></value>
	<value id="wr1EnergyValue">33455.23 kWh</value>
	<value id="wr2EnergyValue">0.00 kWh</value>
	<value id="wr3EnergyValue">0.00 kWh</value>
	<value id="wr4EnergyValue">0.00 kWh</value>
	<value id="wr5EnergyValue">0.00 kWh</value>
	<value id="wpThermEnergyHeatValue">0 kWh</value>
	<value id="wpThermEnergyWaterValue">0 kWh</value>
	<value id="wpTempReturnValue">0.0 &#176;C</value>
	<value id="wpTempWarmWaterValue2">0 &#176;C</value>
	<value id="wpImpTempOutsideValue">0 &#176;C</value>
	<value id="wpThermEnergyPoolValue">0 kWh</value>
	<value id="wpStateValue">Aus</value>
	<value id="wpHeatPumpControlValue">Nicht Aktiv</value>
	<value id="wpIdmTempOutsideValue">0.0 &#176;C</value>
	<value id="hidWpInfo">asdf</value>
	<value id="wpPowerValue">0.00</value>
	<value id="wpEnergyValue"> kWh</value>
	<value id="wpThermPowerValue">0.00 kW</value>
	<value id="wpThermEnergyValue"> kWh</value>
	<value id="wpTempBufferValue">0.0 &#176;C</value>
	<value id="wpTempWarmWaterValue">0.0 &#176;C</value>
	<value id="wpIdmTempOutsideValue">0.0 &#176;C</value>
	<value id="htFirmwareVersion">0</value>
	<value id="htHardwareIdValue">0</value>
	<value id="htSerialOtpValue">0</value>
	<value id="htPowerModeValue">AUS</value>
	<value id="htPowerOutputValue">0.0 %</value>
	<value id="htFixTemperatureValue">0 °C</value>
	<value id="htRTrimValue">0</value>
	<value id="ht4-20mAInputValue">0 %</value>
	<value id="htOutputCtrlStateValue">OUTP_NO_CTRL</value>
	<value id="htRelayStateValue">0</value>
	<value id="htPowerMeasValue">0.00 kW</value>
	<value id="htL1CurrentValue">0 mA</value>
	<value id="htL2CurrentValue">0 mA</value>
	<value id="htL3CurrentValue">0 mA</value>
	<value id="htDipSwitchStandAloneValue">0</value>
	<value id="htDeviceOnTimeValue">0 s</value>
	<value id="htDeviceControlOutputOnTimeValue">0 s</value>
	<value id="htTimeSinceLastRestartValue">0 s</value>
	<value id="htSwitchCounterRelay1Value">0</value>
	<value id="htSwitchCounterRelay2Value">0</value>
	<value id="htSwitchCounterRelay3Value">0</value>
	<value id="htSwitchCounterRelay4Value">0</value>
	<value id="htSwitchCounterRelay5Value">0</value>
	<value id="htSwitchCounterRelay6Value">0</value>
	<value id="htSwitchCounterRelay7Value">0</value>
	<value id="htSwitchCounterRelay8Value">0</value>
	<value id="htSwitchCounterRelay9Value">0</value>
	<value id="htStartSelfTestValue">0</value>
	<value id="htResultSelfTestValue">0</value>
	<value id="htPT1000AValue">0.0 °C</value>
	<value id="htPT1000BValue">0.0 °C</value>
	<value id="htRefVoltageValue">0 V</value>
	<value id="hidhtGlobalUpdateFlag">0</value>
	<value id="hidhtUpdatePercent">0.0 %</value>
	<value id="hidPowerMode">0</value>
	<value id="htTimerTemperatureValue">[[0,0,0]]</value>
	<value id="hidhtUpdateDownloadFlag">0</value>
	<value id="hidEmProd">0</value>
	<value id="hidWrSt1">-1</value>
	<value id="hidWrSt2">-1</value>
	<value id="hidWrSt3">-1</value>
	<value id="hidWrSt4">-1</value>
	<value id="hidWrSt5">-1</value>
	<value id="hidWrConnTimeout1">6</value>
	<value id="hidWrConnTimeout2">0</value>
	<value id="hidWrConnTimeout3">0</value>
	<value id="hidWrConnTimeout4">0</value>
	<value id="hidWrConnTimeout5">0</value>
	<value id="hidWrProd1">9</value>
	<value id="hidWrProd2">0</value>
	<value id="hidWrProd3">0</value>
	<value id="hidWrProd4">0</value>
	<value id="hidWrProd5">0</value>
	<value id="s01Value">0</value>
	<value id="s02Value">0</value>
	<value id="s03Value">0</value>
	<value id="s04Value">0</value>
	<value id="s05Value">0</value>
	<value id="cc1Power">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="cc2Power">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="cc3Power">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="cc4Power">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="cc5Power">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="cc1LastChargeValue">0.00 kWh</value>
	<value id="cc2LastChargeValue">0.00 kWh</value>
	<value id="cc3LastChargeValue">0.00 kWh</value>
	<value id="cc4LastChargeValue">0.00 kWh</value>
	<value id="cc5LastChargeValue">0.00 kWh</value>
	<value id="hidTempsens">0</value>
	<value id="hidLoginEnabled">0</value>
	<value id="userPassword">1509442</value>
	<value id="installerPassword"></value>
	<value id="hidActPrice">32767</value>
	<value id="hidOnTimeAout">0</value>
	<value id="hidOnTimesCC1">0</value>
	<value id="hidOnTimesCC2">0</value>
	<value id="hidOnTimesCC3">0</value>
	<value id="hidOnTimesCC4">0</value>
	<value id="hidOnTimesCC5">0</value>
	<value id="hidSdCardInserted">1</value>
	<value id="hidSD">1</value>
	<value id="hidSdFreeMemory">14268</value>
	<value id="hidAoutPercentage">0</value>
	<value id="hidAoutRemTimeSwitch">0</value>
	<value id="hidAoutRemTimer">0</value>
	<value id="hidR1Status">1</value>
	<value id="hidR2Status">0</value>
	<value id="hidR3Status">0</value>
	<value id="hidR4Status">0</value>
	<value id="hidR1Name">Boiler</value>
	<value id="hidR2Name">Relais</value>
	<value id="hidR3Name">Relais</value>
	<value id="hidR4Name">Trockner</value>
	<value id="hidR1Type">2</value>
	<value id="hidR2Type">0</value>
	<value id="hidR3Type">0</value>
	<value id="hidR4Type">2</value>
	<value id="hidR1Info">2</value>
	<value id="hidR2Info">9</value>
	<value id="hidR3Info">9</value>
	<value id="hidR4Info">0</value>
	<value id="hidR1RemTimeSwitch">566 min</value>
	<value id="hidR2RemTimeSwitch">0 min</value>
	<value id="hidR3RemTimeSwitch">0 min</value>
	<value id="hidR4RemTimeSwitch">65274 min</value>
	<value id="hidR1RemTimer">0</value>
	<value id="hidR2RemTimer">0</value>
	<value id="hidR3RemTimer">0</value>
	<value id="hidR4RemTimer">0</value>
	<value id="hidRelay1Activated">1</value>
	<value id="hidRelay2Activated">0</value>
	<value id="hidRelay3Activated">0</value>
	<value id="hidRelay4Activated">1</value>
	<value id="hidR1Mode">1</value>
	<value id="hidR2Mode">0</value>
	<value id="hidR3Mode">0</value>
	<value id="hidR4Mode">0</value>
	<value id="hidR1Icon">device_heizstab</value>
	<value id="hidR2Icon">device_verbraucher_allg</value>
	<value id="hidR3Icon">device_verbraucher_allg</value>
	<value id="hidR4Icon">device_verbraucher_allg</value>
	<value id="hidProduction">3.98 kW</value>
	<value id="hidPower">510 W</value>
	<value id="batterySoc">-1&#x25;</value>
	<value id="battery1Soc">-1&#x25;</value>
	<value id="battery1Power">0.00 kW</value>
	<value id="battery1Temperature">0 &#176;C</value>
	<value id="bs1CustomerName">Plenticore</value>
	<value id="relais1State">EIN</value>
	<value id="relais2State">AUS</value>
	<value id="relais3State">AUS</value>
	<value id="relais4State">AUS</value>
	<value id="hidBsProd">3</value>
	<value id="hidToGridEnergyDay">5239</value>
	<value id="hidFromGridEnergyDay">2495</value>
	<value id="hidAoutEnergyDay">0</value>
	<value id="hidWr1EnergyDay">8957</value>
	<value id="hidWr2EnergyDay">0</value>
	<value id="hidWr3EnergyDay">0</value>
	<value id="hidWr4EnergyDay">0</value>
	<value id="hidWr5EnergyDay">0</value>
	<value id="hidWpProd">0</value>
	<value id="hidWpElEnergyDay">0</value>
	<value id="hidWpThWaterEnergyDay">0</value>
	<value id="hidWpThHeatEnergyDay">0</value>
	<value id="hidWpThPoolEnergyDay">0</value>
	<value id="hidEm1EnergyFor">0.00</value>
	<value id="hidEm2EnergyFor">0.00</value>
	<value id="hidEm3EnergyFor">0.00</value>
	<value id="hidEm4EnergyFor">0.00</value>
	<value id="hidEm5EnergyFor">0.00</value>
	<value id="hidEm1EnergyRev">0.00</value>
	<value id="hidEm2EnergyRev">0.00</value>
	<value id="hidEm3EnergyRev">0.00</value>
	<value id="hidEm4EnergyRev">0.00</value>
	<value id="hidEm5EnergyRev">0.00</value>
	<value id="hidEm1EnergyDayFor">0.00</value>
	<value id="hidEm2EnergyDayFor">0.00</value>
	<value id="hidEm3EnergyDayFor">0.00</value>
	<value id="hidEm4EnergyDayFor">0.00</value>
	<value id="hidEm5EnergyDayFor">0.00</value>
	<value id="hidEm1EnergyDayRev">0.00</value>
	<value id="hidEm2EnergyDayRev">0.00</value>
	<value id="hidEm3EnergyDayRev">0.00</value>
	<value id="hidEm4EnergyDayRev">0.00</value>
	<value id="hidEm5EnergyDayRev">0.00</value>
	<value id="hidSmartfoxCounter1Setup">0</value>
	<value id="hidSmartfoxCounter2Setup">0</value>
	<value id="hidSmartfoxCounter3Setup">0</value>
	<value id="hidSmartfoxCounter4Setup">0</value>
	<value id="hidSmartfoxCounter5Setup">0</value>
	<value id="hidEmPhaseCurrent">[[0.0,0.0,0.0],[0.0,0.0,0.0],[0.0,0.0,0.0],[0.0,0.0,0.0],[0.0,0.0,0.0]]</value>
	<value id="hidEmConnTimeout1">0</value>
	<value id="hidEmConnTimeout2">0</value>
	<value id="hidEmConnTimeout3">0</value>
	<value id="hidEmConnTimeout4">0</value>
	<value id="hidEmConnTimeout5">0</value>
	<value id="hidSmartfoxCharger1Setup">0</value>
	<value id="hidSmartfoxCharger2Setup">0</value>
	<value id="hidSmartfoxCharger3Setup">0</value>
	<value id="hidSmartfoxCharger4Setup">0</value>
	<value id="hidSmartfoxCharger5Setup">0</value>
	<value id="hidExternalMeter1Type">0</value>
	<value id="hidExternalMeter2Type">0</value>
	<value id="hidExternalMeter3Type">0</value>
	<value id="hidExternalMeter4Type">0</value>
	<value id="hidExternalMeter5Type">0</value>
	<value id="hidExternalMeter1SmartfoxRegister">0</value>
	<value id="hidExternalMeter2SmartfoxRegister">0</value>
	<value id="hidExternalMeter3SmartfoxRegister">0</value>
	<value id="hidExternalMeter4SmartfoxRegister">0</value>
	<value id="hidExternalMeter5SmartfoxRegister">0</value>
	<value id="hidExternalMeter1Name">EM</value>
	<value id="hidExternalMeter2Name">EM</value>
	<value id="hidExternalMeter3Name">EM</value>
	<value id="hidExternalMeter4Name">EM</value>
	<value id="hidExternalMeter5Name">EM</value>
	<value id="externalMeter1Power">0.00 kW</value>
	<value id="externalMeter2Power">0.00 kW</value>
	<value id="externalMeter3Power">0.00 kW</value>
	<value id="externalMeter4Power">0.00 kW</value>
	<value id="externalMeter5Power">0.00 kW</value>
	<value id="hidConsumptionController">0</value>
	<value id="hidS0InputType">0</value>
	<value id="hidS0InputValue">0.00</value>
	<value id="hidS0InputUnit"></value>
	<value id="hidS0InputDayPulses">nan</value>
	<value id="hidS0InputName"></value>
	<value id="S0InputTotalPulses">0</value>
	<value id="CC_Prio_Infos">firstPrio: 0
		<br/>lastPrio: 0
		<br/>powerScope: 0
		<br/>currentScope: 0
		<br/>prioMaxValue: 0, 0, 0, 0, 0, 0
		<br/>prioMinValue: 0, 0, 0, 0, 0, 0
		<br/>prioCounters: 0, 0, 0, 0, 0, 0
	</value>
	<value id="consumptionControl1Header">VB</value>
	<value id="consumptionControl1Percent">0%</value>
	<value id="consumptionControl1RealPercent">0.0%</value>
	<value id="consumptionControl1TimerPercent">0.0%</value>
	<value id="consumptionControl1Power">0.00 &lt;span&gt;kW&lt;/span&gt;</value>
	<value id="consumptionControl1EnergyDay">0</value>
	<value id="consumptionControl1Temp">0.0°C</value>
	<value id="hidConsumptionControl1Mode">2</value>
	<value id="hidConsumptionControl1Percentage">0</value>
	<value id="hidConsumptionControl1RemTimer">0</value>
	<value id="hidConsumptionControlConnTimeout1">0</value>
	<value id="hidConsumptionControl1State">0</value>
	<value id="hidConsumptionControl1Info">1</value>
	<value id="hidConsumptionControl1Description">VB</value>
	<value id="hidConsumptionControl1StatusText"></value>
	<value id="hidConsumptionControl1CLOCK_STATE">0</value>
	<value id="hidConsumptionControl1RemTimeSwitch">0</value>
	<value id="consumptionModalpHHygieneMode">0</value>
	<value id="consumptionModalpHHygieneStarttime">00:00</value>
	<value id="consumptionModalpHHygieneDuration">0</value>
	<value id="consumptionModalpHHygieneTemperatur">0</value>
	<value id="consumptionModalpHHygieneIntervall">0</value>
	<value id="hidTestLicDaysInverter">0</value>
	<value id="hidTestLicDaysHeatPump">0</value>
	<value id="hidTestLicDaysBattery">0</value>
	<value id="hidTestLicDaysCarCharger">359</value>
	<value id="hidEnergyTariffActivated">0</value>
	<value id="inverter1ConfigPaneIp">192.168.000.231</value>
	<value id="inverter1ConfigPaneModbus">71</value>
	<value id="inverter2ConfigPaneIp">000.000.000.000</value>
	<value id="inverter2ConfigPaneModbus">255</value>
	<value id="inverter3ConfigPaneIp">000.000.000.000</value>
	<value id="inverter3ConfigPaneModbus">255</value>
	<value id="inverter4ConfigPaneIp">000.000.000.000</value>
	<value id="inverter4ConfigPaneModbus">255</value>
	<value id="inverter5ConfigPaneIp">000.000.000.000</value>
	<value id="inverter5ConfigPaneModbus">255</value>
	<value id="consumptionControlConfigPane1Name">VB</value>
	<value id="consumptionControlConfigPane1Ip">000.000.000.000</value>
	<value id="consumptionControlConfigPane1Rtu">40</value>
	<value id="externalMeterConfigPane1Name">EM</value>
	<value id="externalMeterConfigPane1Ip">000.168.000.040</value>
	<value id="externalMeterConfigPane1Modbus">1</value>
	<value id="externalMeterConfigPane2Name">EM</value>
	<value id="externalMeterConfigPane2Ip">000.000.000.000</value>
	<value id="externalMeterConfigPane2Modbus">1</value>
	<value id="externalMeterConfigPane3Name">EM</value>
	<value id="externalMeterConfigPane3Ip">000.168.000.040</value>
	<value id="externalMeterConfigPane3Modbus">1</value>
	<value id="externalMeterConfigPane4Name">EM</value>
	<value id="externalMeterConfigPane4Ip">000.000.000.000</value>
	<value id="externalMeterConfigPane4Modbus">1</value>
	<value id="externalMeterConfigPane5Name">EM</value>
	<value id="externalMeterConfigPane5Ip">000.000.000.000</value>
	<value id="externalMeterConfigPane5Modbus">1</value>
	<value id="battery1ConfigPaneIp">192.168.001.190</value>
	<value id="carCharger1ConfigPaneIp">192.168.001.210</value>
	<value id="carCharger1ConfigPaneSerial">0</value>
	<value id="carCharger2ConfigPaneIp">000.000.000.000</value>
	<value id="carCharger2ConfigPaneSerial">0</value>
	<value id="carCharger3ConfigPaneIp">000.000.000.000</value>
	<value id="carCharger3ConfigPaneSerial">0</value>
	<value id="carCharger4ConfigPaneIp">000.000.000.000</value>
	<value id="carCharger4ConfigPaneSerial">0</value>
	<value id="carCharger5ConfigPaneIp">000.000.000.000</value>
	<value id="carCharger5ConfigPaneSerial">0</value>
	<value id="hidTcpConverterList">[]</value>
</values>
```

## Calculation of some values

### Live data

```javascript
var e = hiddenValues.hidProduction;
e = e.replace(',', ''),
e = Number(e.replace(' kW', '')) / 100,
e += serverInfoPvPower;
var t = hiddenValues.hidPower;
t = Number(t.replace(' W', '')) / 1e3;
var n,
    d = hiddenValues.battery1Power;
d = d.replace(',', '');
var o;
o = (d = Number(d.replace(' kW', '')) / 100) > 0,
(n = e + t - d) < 0 && (n = 0),
document.getElementById('lineProductionColor').style.display = 'none',
document.getElementById('lineProductionGray').style.display = 'none',
document.getElementById('productionFlowItem').hidden = !0,
document.getElementById('lineConsumptionColor').style.display = 'none',
document.getElementById('lineConsumptionGray').style.display = 'none',
document.getElementById('consumptionFlowItem').hidden = !0,
document.getElementById('lineGridBlue').style.display = 'none',
document.getElementById('fromGridFlowItem').hidden = !0,
document.getElementById('lineGridRed').style.display = 'none',
document.getElementById('toGridFlowItem').hidden = !0,
e > 0 ? (document.getElementById('lineProductionColor').style.display = '', document.getElementById('productionFlowItem').hidden = !1, wasProduction || restartAnimation('productionFlowItem'), wasProduction = !0) : (document.getElementById('lineProductionGray').style.display = '', wasProduction = !1),
checkIfSmartfoxConsumes() ? (document.getElementById('lineConsumptionColor').style.display = '', document.getElementById('consumptionFlowItem').hidden = !1, wasConsumption || restartAnimation('consumptionFlowItem'), wasConsumption = !0) : (document.getElementById('lineConsumptionGray').style.display = '', wasConsumption = !1),
document.getElementById('lineBatteryBrown').style.display = 'none',
document.getElementById('lineBatteryGray').style.display = '',
document.getElementById('batteryChargeFlowItem').hidden = !0,
document.getElementById('batteryDischargeFlowItem').hidden = !0,
document.getElementById('batteryCircle').classList.add('inactive');
var i = document.getElementById('batteryStatusText'),
    r = Number(hiddenValues.hidWithBattery);
0 != d && '' != d && 1 == r ? o ? (i.innerHTML = translate('charging'), document.getElementById('batteryChargeFlowItem').hidden = !1, document.getElementById('batteryDischargeFlowItem').hidden = !0, document.getElementById('lineBatteryBrown').style.display = '', document.getElementById('lineBatteryGray').style.display = 'none', document.getElementById('batteryCircle').classList.remove('inactive')) : (i.innerHTML = translate('discharging'), document.getElementById('batteryChargeFlowItem').hidden = !0, document.getElementById('batteryDischargeFlowItem').hidden = !1, document.getElementById('lineBatteryBrown').style.display = '', document.getElementById('lineBatteryGray').style.display = 'none', document.getElementById('batteryCircle').classList.remove('inactive')) : i.innerHTML = '',
t >= 0 ? (document.getElementById('lineGridBlue').style.display = '', document.getElementById('fromGridFlowItem').hidden = !1, wasfromGrid || restartAnimation('fromGridFlowItem'), wasfromGrid = !0, wasToGrid = !1) : (document.getElementById('lineGridRed').style.display = '', document.getElementById('toGridFlowItem').hidden = !1, wasToGrid || restartAnimation('toGridFlowItem'), wasToGrid = !0, wasfromGrid = !1);
var m = 0,
    l = 100;
e > 0 && (m = 100, l = Math.round(n / e * 100)),
n > 0 || (l = 0),
l > 100 && (l = 100),
document.getElementById('productionValue').innerHTML = e.toFixed(2).replace('.', commaSign) + '<span> kW</span>',
document.getElementById('consumptionValue').innerHTML = n.toFixed(2).replace('.', commaSign) + '<span> kW</span>',
document.getElementById('consumptionPercentValue').innerHTML = l + '%',
document.getElementById('batteryPower').innerHTML = d.toFixed(2).replace('.', commaSign) + '<span> kW</span>',
initExternalMeterValues(useLiveData),
document.getElementById('heatPumpEnergy').innerHTML = hiddenValues.wpEnergyValue,
t >= 0 ? (document.getElementById('powerText').innerHTML = translate('fromGrid'), document.getElementById('powerValue').innerHTML = t.toFixed(2).replace('.', commaSign) + '<span> kW</span>', setPercentageGrid('blue')) : (document.getElementById('powerText').innerHTML = translate('toGrid'), document.getElementById('powerValue').innerHTML = (-1 * t).toFixed(2).replace('.', commaSign) + '<span> kW</span>', setPercentageGrid('red')),
document.getElementById('productionCircle').classList.remove('noAnimation'),
document.getElementById('batteryCircle').classList.remove('noAnimation'),
document.getElementById('consumptionCircle').classList.remove('noAnimation'),
document.getElementById('gridCircle').classList.remove('noAnimation'),
document.getElementById('devicesContainer').classList.remove('noAnimation'),
setPercentageProduction(m),
setPercentageConsumption(l)
```

### Historical data

```javascript
var e = Number(hiddenValues.hidWr1EnergyDay) / 1e3;
e += Number(hiddenValues.hidWr2EnergyDay) / 1e3,
e += Number(hiddenValues.hidWr3EnergyDay) / 1e3,
e += Number(hiddenValues.hidWr4EnergyDay) / 1e3,
e += Number(hiddenValues.hidWr5EnergyDay) / 1e3;
var t = Number(hiddenValues.hidFromGridEnergyDay) / 1e3,
    a = Number(hiddenValues.hidToGridEnergyDay) / 1e3,
    n = Number(hiddenValues.hidAoutEnergyDay) / 1e3,
    o = t - a + e;
o < 0 && (o = 0);
var s = Math.round(o / e * 100);
s > 100 && (s = 100),
isNaN(s) && (s = 0),
document.getElementById('consumptionValue').innerHTML = (o.toFixed(2) + '<span> kWh</span>').replaceAll('.', commaSign),
document.getElementById('consumptionPercentValue').innerHTML = s + '%',
document.getElementById('powerValue').innerHTML = (t.toFixed(1) + ' | ' + a.toFixed(1)).replaceAll('.', commaSign),
document.getElementById('powerText').innerHTML = 'Bezug | Lieferung',
document.getElementById('productionValue').innerHTML = (e.toFixed(2) + '<span> kWh</span>').replaceAll('.', commaSign),
document.getElementById('batteryPower').innerHTML = '--',
document.getElementById('batteryStatusText').innerHTML = '--',
document.getElementById('analogOutPower').innerHTML = (n.toFixed(2) + '<span> kWh</span>').replaceAll('.', commaSign),
document.getElementById('cc1Power').innerHTML = hiddenValues.hidCc1EnergyDay + ' <span> kWh</span>',
document.getElementById('cc2Power').innerHTML = hiddenValues.hidCc2EnergyDay + ' <span> kWh</span>',
document.getElementById('cc3Power').innerHTML = hiddenValues.hidCc3EnergyDay + ' <span> kWh</span>',
document.getElementById('cc4Power').innerHTML = hiddenValues.hidCc4EnergyDay + ' <span> kWh</span>',
document.getElementById('cc5Power').innerHTML = hiddenValues.hidCc5EnergyDay + ' <span> kWh</span>',
document.getElementById('heatPumpPower').innerHTML = hiddenValues.hidWpElEnergyDay + ' <span> kWh</span>',
document.getElementById('wr1EnergyValue').innerHTML = (Number(hiddenValues.hidWr1EnergyDay) / 1e3).toFixed(2) + ' kWh',
document.getElementById('wr2EnergyValue').innerHTML = (Number(hiddenValues.hidWr2EnergyDay) / 1e3).toFixed(2) + ' kWh',
document.getElementById('wr3EnergyValue').innerHTML = (Number(hiddenValues.hidWr3EnergyDay) / 1e3).toFixed(2) + ' kWh',
document.getElementById('wr4EnergyValue').innerHTML = (Number(hiddenValues.hidWr4EnergyDay) / 1e3).toFixed(2) + ' kWh',
document.getElementById('wr5EnergyValue').innerHTML = (Number(hiddenValues.hidWr5EnergyDay) / 1e3).toFixed(2) + ' kWh',
document.getElementById('consumptionControl1Power').innerHTML = (Number(hiddenValues.consumptionControl1EnergyDay) / 1e3).toFixed(2) + ' <span> kWh</span>',
initExternalMeterValues(useLiveData),
document.getElementById('s0InputValue').innerHTML = hiddenValues.hidS0InputDayPulses + ' <span> kWh</span>',
document.getElementById('productionCircle').classList.add('noAnimation'),
document.getElementById('batteryCircle').classList.add('noAnimation'),
document.getElementById('batteryCircle').classList.remove('inactive'),
document.getElementById('batteryCircle').classList.add('active'),
document.getElementById('consumptionCircle').classList.add('noAnimation'),
document.getElementById('gridCircle').classList.add('noAnimation'),
document.getElementById('devicesContainer').classList.add('noAnimation'),
document.getElementById('lineProductionColor').style.display = '',
document.getElementById('lineProductionGray').style.display = 'none',
document.getElementById('lineConsumptionColor').style.display = 'none',
document.getElementById('lineConsumptionGray').style.display = '',
o > 0 && (document.getElementById('lineConsumptionColor').style.display = '', document.getElementById('lineConsumptionGray').style.display = 'none'),
t > a ? (document.getElementById('lineGridBlue').style.display = '', document.getElementById('lineGridRed').style.display = 'none', setPercentageGrid('blue')) : (document.getElementById('lineGridBlue').style.display = 'none', document.getElementById('lineGridRed').style.display = '', setPercentageGrid('red')),
document.getElementById('lineBatteryBrown').style.display = '',
document.getElementById('lineBatteryGray').style.display = 'none',
document.getElementById('batteryChargeFlowItem').hidden = !0,
document.getElementById('batteryDischargeFlowItem').hidden = !0,
document.getElementById('fromGridFlowItem').hidden = !0,
document.getElementById('toGridFlowItem').hidden = !0,
document.getElementById('productionFlowItem').hidden = !0,
document.getElementById('consumptionFlowItem').hidden = !0,
hideModal('loadingModal'),
setPercentageProduction(100),
setPercentageConsumption(s)
```