Readme file for Aurora version 4.2

*** Important INFO ***
The Aurora plugins are XFM modules, not VST plugins. Hence they are not to be
copied inside the subdirectories named "vstplugins" or "Plug-ins", instead the 
Aurora modules have to be copied in the "main" directory of Audition.
As a general rule, never enable the Windows option "hide extension for known file types": 
it is always suggested to display the extension for any file.

Registered users will receive one or more TXT files, containing the registration
codes: these files should be copied in C:\Windows, or in any other directory
being part of the PATH of your system. The TXT registration files should NOT be
placed in the Audition directory.

Aurora was developed on an English version of Windows, set up with English regional 
parameters: it cannot be ensured that all the capabilities of Aurora are fully 
operational when different regional settings are employed, particularly regarding 
the export of results to data tables, either through the Windows clipboard or
through ASCII txt files. As a general rule, avoid nationalized versions of the OS,
programs and plugins. Particularly harmful are the nationalized versions of Audition,
which are translated really badly (at least, the Italian version is almost unusable).
Please, learn English, and always use it for everything.... 

*** Aurora 4.2 ***
The following plugins have been updated, with bug fixes and additional features:
Acoustic42.xfm
Convolv.xfm
Gensweep.xfm
Kirkeby4.xfm
IRselect.xfm
ITUP56.xfm
Sti.xfm
Syncavg.xfm
XFunction.xfm
The modules with more relevant modifications were: 
* Acoustical parameters, now including visualization of the octave-band spectrum 
of each parameter
* Gensweep, now including proper choice of fade-in and fade-out windows, which
are applied also to the inverse sweep
* Kirkeby4, (actually v. 4.3 beta) which now includes also an "Indipendent Stereo" 
mode for separate inversion of the two channels of a stereo system (without 
cross-talk cancellation) and the multiple inversion of a (large) number of 
consecutive IRs, all of the same lenght, very useful for equalizing loudspeaker 
or microphone arrays. The 4.3 Beta version includes even fade-in and fade-out of
the original IR to be inverted, for avoiding "edge effects"
* ITUP56, now displays and computes the parameters of the average of the two
input channels
* Cross Functions, now it computes correctly the unnormalized transfer function,
and can create a "reference" Dirac delta pulse on the right channel.
The remaining plugins are not modified

Attention! the Acoustical Parameters plugin is now named Acoustic42.XFM, while the 
previous one was named Acoustic4.XFM, so this is not overwrittem when copying
the new plugins to the Audition directory. This results in both plugins appearing
in the menus. If you do not need anymore the older version, please delete the file
named Acoustics4.xfm from your Audition directory.
Aurora 4.2 has been tested to be fully functional also under Audobe Audition 3.0
Due to the number of bugs found in Audition 2.0, it is now recommended to all Aurora
users to upgrade to Audition 3.0, or to stay with the old Audition 1.5. Support
for users of Audition 2.0 has been withdrawn, and Aurora is not declared anymore 
suitable for that crappy version of Audition.

*** Aurora 4.1 ***
The following plugins have been updated, with bug fixes and additional features:
Acoustic4.xfm
Kirkeby4.xfm
ITUP56.xfm
Sti.xfm
XFunction.xfm
The bigger modifications are in XFunction, which now contains the possibility to employ a 
pressure-velocity (Microflown) probe for measurement of the absorption coefficient and acoustical
impedance of surfaces, both inside a standing-wave tube and in free-field.
See the forthcoming paper being presente at ICSV-13 for more details. 
The manual will be updated in the future...
Aurora 4.1 has been tested to be fully functional also under Adobe Audition 2.0.

*** Aurora 4.0 ***
Aurora 4.0 is the first major upgrade of the Aurora package in 5 years. It is released
as stable version (not Beta), equipped with complete Help file and tested working
correctly under the new host program Adobe Audition (either version 1.0 or 1.5).
The modules now take advantage of the new capabilities of Audition, such as Spectral Editing.
Furthermore, two brand-new modules have been included: STI (speech Transmission Index)
and ITU-P56 (Time History Analysis) - for both modules, read the help file for more
information and a functional description.
Several obsolete or unstable modules have been dropped, now Aurora 4.0 consists of 16 XFM
plugins plus the MLSSA tim file filter.


*** Aurora 3.3 beta1 release ***
4 plugins have been substantially modified:
- Convolv.xfm, now compiled with the new, ultra-fast intel IPP FFT libraries. The 
convolution is now incredibly fast, and the "preview" button has been added for
realtime listening of the convolution effect.
- Gensweep.xfm: now the pulse on the right channel which controls the advancement 
of the rotating table has been placed in the middle of the silence gap between one 
sweep and the next.
- IRselect. This is a new plugin, whih substitutes the "Synchronous Average" for 
measurement sets made without repetitions of the sine sweep. It does not employ anymore
the Windows clipboard, teh results are left on the currently displayed waveform.
- Kirkeby2. Now frequency-domain "smoothing" is possible prior of the inversion...
Aurora 3.3 has been verified to work perfectly under Cool Edit Pro 2.1 ...

*** Aurora 3.2 Beta 8 modifications ***
Verified perfect compatibility with Windows XP and with CoolEditPro v. 2.0a

*** Beta 7 modifications ***
Three plugins neeede to be recompiled for gaining full compatibility with the
new release of CoolEdit, called Cool Edit Pro 2.0.
The three plugins are Convolve with clipboard, ConvoWarp and Deconvolve IRS/Clip
All these three plugins needed to get data from the Windows clipboard, and now CEP2
changed the format for storing 32-bits waveforms on the clipboard.
All other plugins are unaffected.

*** Alpha-stage plugins ***
The new Cross-Functions (Xfunction.xfm) module has been released. This module only
works on stereo waveforms, and it can compute the two autocorrelations, the cross
correlation, and the transfer functions H1, H2 and H3. Furthermore, the result can
be viewed as envelope through a squared Hilbert transform.
Finally, a frequency-domain following filter is optionally activated. This tracks
the peak frequency of one of the two channels, and filters only a specified bandwidth
around this frequency. This can greatly improve the S/N ratio for measurements
conducted with sine sweep as excitation signal.
The GenSweep module now can also create the time reversal of the inverse filter directly
on the right channel. This can be useful when the new Cross Functions module is employed
because this way a simple cross-correlation between the system response and the time-
reversal of the excitation signal yields the impulse response, without the known
problems associated with the H1, H2 and H3 estimators.
In this case, the normal operational way is to loopback the right output channel to the
left input channel, to drive the loudspeaker with the Left output channel, and to
connect the microphone to the right input channel. 
If this cannot be done, and the right output must necessarily be looped back to the right
input, the X-functions module contains a specific "Time Reversal" flag, which restores
the correct orientation of the time axis after a cross-correlation with the channels
having been swapped.
Finally, a very-Beta (or Alpha, if You prefer) version of the forthcoming Acoustical Paramater
module has been added. It is called Acoustic_32.xfm, and it is now capable also of 1/3
octave computations. Please note that the 1/3 octave results are accurate only if the
sampling rate was 44.1 kHz (wee are working on extending this limit).
Furthermore, the module can now compute also the ANDO parameters (IACC-based) and the ISO3382
spatiality indicators (LF, LFC). The first values are meaningful only if the processed
signal was a Binaural Impulse response (BIR), measured with a dummy head. The other
spatiality parameters require instead the use of a Soundfield microphone in WY mode,
or that the left channel is driven by an omni, and the right channel by a figure-of-8.
Everything in this new module is not very stable yet, we cannot claim this module to be
in Beta stage...

*** Beta 6 modifications ***
Other improvements to the Acoustical Parameters module. Now the graphical display is
more correct, closely resembling what is done by the MLSSA software. The calculation
of energetic ratios (Clarity, Definition) was improved, taking into account the 
response time of the octave-band filters, as suggested in the appendix of the
ISO3382/1997 standard. This is particularly relevant at the lower frequency bands.

*** Beta 5 modifications ***
The Generate Multiple MLS signal module was substantially improved. Now it is possible
to repeat the MLS sequence several times, wich is very useful for measurements
made with a rotating table. The sync pulse for activating the rotating board can now 
be synced at the beginning or at the end of each repetition.

*** Beta 4 modifications ***
Some aesthetic improvements and bug fixes to Acoustical Parameters module.

*** Beta 3 main improvements ***
1) All the modules now respond to CoolEdit with XFMValidLibrary=1157, which enables
them to work both under CoolEditPro and CoolEdit2000. The support for Cool96 is
no more available.
2) Improved robustness of all the modules, except for Real Time Convolver, who still
crashes after too many button pressures on the module's interface.

*** Beta 2 main improvements ***
1) Now Calculate Acoustics has a beatiful graphical interface for displaying
the Impulse Response (in dB scale) superposed with the Schroeder plot. It is
possible to display how the impulse response changes when filtered in each
octave band.
2) Now also Signal and Noise level are shown. The value is expressed in terms
of SEL (Single Event Level), and thus represent the total energy of the 
Impulse Response. This value corresponds with teh starting point of the
Schroeder plot. Instead, the Impulse Response plot is scaled in 
"Instantaneous dB", with an RMS integration time equal to 1/500 of the
Impulse Response length
3) The new parameter Strength is computed. This requires that a reference
free-field impulse response has been previously stored as reference level.
4) The Invert Kirkeby module now also supports a simplified Cross-talk cancel
only mode, (from an original idea of Ralph Glasgal), which computes cross
talk cancelling filters without any equalization on the ipselateral paths.
5) The MLSSA tim filter now maintains 32-bits depth also during the export.

*** Aurora 3.2 BETA main improvements ***
1) All the modules now are compliant with 32-bit waveform processing, without
any intermediate reduction to 16 bits during data transfers between CoolEdit
and the plugins. This results in improved dynamic range and reduced computational
noise.
2) Some minor bugs have been corrected in many modules.
3) The new module ConvoWarp has been added, implementing WFIR processing (Warped
Finite Impulse Response filtering). Also cross-talk cancelling networks, with 4
separate filters (in the 2x2 format) are accepted.
4) The Invert Kirkeby module now accepts the computation of filters shorter than
the original impulse responses to invert. This has been done with the new Mourjopoulos
formulation of frequency-domain smoothing (AES Journal, March 2000), which indirectly
causes the computation of the inverse filters to be made with an algorithm which is
substantially different from the original Nelson-Kirkeby formulation, because now not
only the regularization parameter is variable with frequency, but also the equivalent
bandwidth of each spectral line is variable with approximate logarithmic law.


*** Setup Instructions ***

In this directory the whole set of Aurora plug-ins for CoolEdit
is stored. The plug-ins are in the ZIP files called AURORA32BETA2.zip 
(Aurora 3.2 Beta2, released on 06/september/2000). 
No installation procedure is required: simply copy the contents of the
ZIP file within the directory where the CoolEdit Program was installed.
If CoolEdit seems to not recognize the new modules, simply destroy
the files called XFM.DAT and FLT.DAT. At the subsequent launch, CoolEdit
will scan for new plug-ins and recreate the above two files.

Registration of Aurora plug-ins.
These plugins are not registered, You can use them only for evaluation.
If You want to register, please contact the new publisher (KAGI.COM) 
who is now ready to accept on-line registration.
The unregistered plug-ins are fully functional, but they exhibit an 
annoying behaviour. Randomly (with a chance of 1:4) they crash CoolEdit!
Of course, after registration this annoying behaviour disappears...

Self-Registration of Aurora 3.2 plugins
The new release of Aurora 3.2 introduces self-registration of the
plugins. If You received Your username and reg.key from Acoustec, simply
create a text file called AuroKey.txt, containing in the first line
Your username, and the reg.key in the second line. Save this file in any 
directory in your PATH (i.e. C:\Windows). Then destroy the file XFM.DAT
in the CoolEdit directory, so that CoolEdit is forced to re-inizialize
the plugins at the next start. Each plugin will search for the AuroKey.txt
file, and if found will read automatically the reg.info from it.

Aurora 3.2 single-plugin self registration
If You only purchased some of the 16 plugins, You will receive a separate 
TXT file for each plugin (acoustic.txt, convolv.txt, etc.). AGain, You need
to copy all these files in a directory included in Your PATH string.

Help Files
The help files and the manual included are out-of-date with the
current development of plug-ins. Together with the official release of
Aurora 3.2 (scheduled for 30th September 2000), updated help files, in English, 
will be available on this site.
For the manual a couple of months more will be required...
In the meanwhile, please refer to the Aurora web pages for explanations.

Enjoy it!

Angelo Farina