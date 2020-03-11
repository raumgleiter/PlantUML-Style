# PlantUML | Deployment Diagram

``` plantuml
@startuml
!define STYLE_RG
!include <tupadr3/common>
!include <tupadr3/font-awesome-5/rocket>
!include <tupadr3/font-awesome-5/phone>
!include <tupadr3/font-awesome-5/user>














'******************************************************************************

!ifndef FONTNAME
!define FONTNAME "sans-serif"
!endif

!ifndef FONTSIZE
!define FONTSIZE 11
!endif

'-----------------------------------------------------------------------------

!define DarkRed 8B0000
!define Teal 008080
!define DarkGreen 006400
!define MidnightBlue 191970
!define DarkSlateBlue 483D8B
!define Sienna A0522D
!define DarkGoldenrod B8860B
!define MediumVioletRed C71585
!define OliveDrab 6B8E23
!define DarkOliveGreen 556B2F

'-----------------------------------------------------------------------------

!ifdef STYLE_RG
!define ACCENT fff
!define ACCENTDARK 333
skinparam stereotypeCBackgroundColor ACCENTDARK
!define PRIMARY 000
!define SECONDARY 333
!define ARROWCOLOR 666
!define ARROWFONTCOLOR 333
!define BORDERCOLOR fff
!define BOXBG ccc
!define BACKGROUND fff
skinparam backgroundColor BACKGROUND
!endif

'-----------------------------------------------------------------------------
'-----------------------------------------------------------------------------

'******************************************************************************

'-----------------------------------------------------------------------------


'-----------------------------------------------------------------------------
'-----------------------------------------------------------------------------

'******************************************************************************

'-----------------------------------------------------------------------------

!function font_style()
  fontColor PRIMARY
  fontName FONTNAME
  fontSize FONTSIZE
  stereotypeFontColor SECONDARY
  stereotypeFontSize FONTSIZE
!endfunction

!function color_style()
  fontColor<<RED>> DarkRed
  fontColor<<TEAL>> Teal
  fontColor<<GREEN>> DarkGreen
  fontColor<<BLUE>> MidnightBlue
  fontColor<<PURPLE>> DarkSlateBlue
  fontColor<<ORANGE>> Sienna
  fontColor<<GOLD>> DarkGoldenrod
  fontColor<<VIOLET>> MediumVioletRed
  fontColor<<OLIVE>> DarkOliveGreen
!endfunction

!function basic_style()
  color_style()
  backgroundColor BOXBG
  borderColor BORDERCOLOR
!endfunction

!function hidden_style()
  color_style()
  backgroundColor BACKGROUND
  borderColor BOXBG
  'borderColor BACKGROUND
!endfunction

!function accent_style()
  backgroundColor ACCENT
  borderColor ACCENTDARK
!endfunction

!function arrow_style()
  arrowColor ARROWCOLOR
  arrowFontName FONTNAME
  arrowFontColor ARROWFONTCOLOR
  arrowFontSize FONTSIZE
!endfunction

' Class diagrams

skinparam circledCharacter {
  radius 8
  fontSize FONTSIZE
  fontName FONTNAME
}

skinparam class {
  basic_style()
  font_style()
  arrow_style()

  attributeFontColor SECONDARY
  attributeFontSize FONTSIZE
  attributeIconSize FONTSIZE
}

' Sequence diagrams

skinparam actor {
  accent_style()
  font_style()
}

skinparam participant {
  basic_style()
  font_style()
}

' Component diagrams

skinparam interface {
  accent_style()
  font_style()
}

skinparam component {
  basic_style()
  font_style()
}

skinparam agent {
  basic_style()
  font_style()
}

skinparam artifact {
  accent_style()
  font_style()
}

skinparam stack {
  basic_style()
  font_style()
}

skinparam package {
  basic_style()
  font_style()
}

skinparam file {
  basic_style()
  font_style()
}

skinparam card {
  hidden_style()
  font_style()
  defaultTextAlignment center
}

skinparam iframe {
  basic_style()
  font_style()
}

skinparam frame {
  basic_style()
  font_style()
}

skinparam folder {
  basic_style()
  font_style()
}

skinparam node {
  basic_style()
  font_style()
}

skinparam database {
  basic_style()
  font_style()
}

skinparam queue {
  basic_style()
  font_style()
}

' Use Case diagrams

skinparam usecase {
  hidden_style()
  font_style()
  arrow_style()
}

skinparam activity {
  basic_style()
  font_style()
  arrow_style()
}

skinparam sequence {
  font_style()
  arrow_style()

  lifeLineBorderColor ARROWCOLOR
  lifeLineBackgroundColor ARROWFONTCOLOR
}

skinparam boundary {
  accent_style()
  font_style()
}

skinparam control {
  accent_style()
  font_style()
}

skinparam entity {
  accent_style()
  font_style()
}

' State diagrams

skinparam state {
  basic_style()
  font_style()
  arrow_style()
  startColor ACCENT
  endColor ACCENTDARK
}

' Object diagrams

skinparam object {
  basic_style()
  font_style()
  arrow_style()
}

' Common

skinparam note {
  accent_style()
  font_style()
}

skinparam cloud {
  basic_style()
  font_style()
  arrow_style()
}

skinparam rectangle {
  accent_style()
  font_style()
}

skinparam storage {
  basic_style()
  font_style()
}


















'******************************************************************************

skinparam defaultTextAlignment center

actor actor
agent agent
artifact artifact
boundary boundary
card card
cloud cloud
component component
control control
database database
entity entity
file file
folder folder
frame frame
interface  interface
node node
package package
queue queue
stack stack
rectangle rectangle
storage storage
usecase usecase

database database_pretty [
  <$rocket>
  Rockets rock!
]
card card_pretty [
  <$phone>
  Call me!
]
usecase usecase_complex<<OLIVE>> [
  <$phone>
  Call me!
  ---
  Where?
  on my cellphone
]
usecase usecase_pretty<<GREEN>> [
  <$phone>
  Call me!
]

actor --> database_pretty

artifact Foo1 {
  folder Foo2
}
rectangle Foo7 {
  agent Foo8
}
folder Foo3 {
  artifact Foo4
}
cloud Foo5 {
  card Foo6
}
cloud vpc {
  node ec2 {
	stack stacky
  }
}



'-----------------------------------------------------------------------------
'-----------------------------------------------------------------------------

@enduml
```
