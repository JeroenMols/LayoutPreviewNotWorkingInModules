# Layout preview not working when custom view is inclued in xml of submodule
Reproduction project for Android studio bug

## Scenario
a custom view of two textviews (title & subtitle), created by inflating a layout resource in init method of a custom subclass of LinearLayout. 
- In the main app module: including that custom view in another layout xml file (`preview_working.xml), the layout preview works.
- In a submodule: including that custom view in another layout xml file (`preview_not_working.xml), the layout preview does not work.

Expected result: Layout previews for custom ViewGroups always work, both for inclusions into layout files in the main app module and in submodules.

Actual result: Layout previews for custom ViewGroups only work when included into a layout file in the main app module. They don't work when it is included into a layout file in a submodule.

## Environment
Android Studio 3.3 Beta 4

Build #AI-182.4892.20.33.5114240, built on November 6, 2018

JRE: 1.8.0_152-release-1248-b01 x86_64

JVM: OpenJDK 64-Bit Server VM by JetBrains s.r.o

macOS 10.13.3
