# Non-linearity of a systme:
1.amplitude depended transconductance
  At small signal levels, gm is roughly constant.
  As the signal becomes larger, the device moves into regions where gm changes with input amplitude.
  Result: The output current does not increase perfectly in proportion to the input signal → nonlinearity.
2.Parasitic elements that change with signal amplitude
  Real devices contain parasitic capacitances and resistances (e.g., junction capacitance in a transistor). These parasitics:
  Do not stay constant
  Change with voltage or current level
  For example:
  Diode junction capacitance shrinks as reverse voltage increases.
  MOSFET capacitances vary depending on gate–source and drain–source voltages.
  Result: The circuit’s frequency response and behavior shift depending on signal amplitude → more nonlinearit
3. Clipping when the signal exceeds allowable swing
  Every circuit has limits on how far the output can swing (due to supply voltages or device limits). If the input signal is      too large:
  Peaks or troughs of the waveform get “cut off”
  This is called clipping
  Clipping is a strong, highly audible/visible form of nonlinearity and introduces a large number of distortion components        (harmonics).

  * Two forms of RF circuit nonlinearity: harmonic distortion and gain compression. We’ll also explore the 1 dB compression point, a useful metric for characterizing gain compression

# What is 1dB compression point?
 the 1 dB compression point is defined as the power level at which output power falls 1 dB below the ideal linear characteristic. We use this specification to quantify the upper limit of an RF circuit’s linear operation.
 <img width="527" height="450" alt="image" src="https://github.com/user-attachments/assets/7d4800da-17b1-49d5-8b43-a4022e94a350" />

* The input compression point of RF receivers is typically in the range of –20 to –25 dBm

Q: What is memoryless system? and memory system?
memoryless system: the output is not depended on the input where the momory system where the ouput is depended on the previous state. (??)



# Modeling a Memoryless Non-linear System
