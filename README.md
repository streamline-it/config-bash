Role Name
=========

Config the bash environment by adding aliases and configuring colors for man and the less command by modifying .bashrc

Requirements
------------

None.

Role Variables
--------------

config_bash_bashrc_filename: ".bashrc"

# users accounts
config_bash_user_accts:
  - name: 
    homedir: 

config_bash_bashrc_lines:
  - line: "alias ls='ls --color=auto'"
    regex: "alias ls="
  - line: "alias ll='ls -lh --color=auto'"
    regex: "alias ll="
  - line: "alias la='ls -ah --color=auto'"
    regex: "alias la="
  - line: "alias l.='ls -d --color=auto"
    regex: "alias l.="

# establish termcap colors
config_bash_color_black: "$'\e[1;30m'"
config_bash_color_red: "$'\e[1;31m'"
config_bash_color_green:  "$'\e[1;32m'"
config_bash_color_yellow: "$'\e[1;33m'"
config_bash_color_blue: "$'\e[1;34m'"
config_bash_color_purple: "$'\e[1;35m'"
config_bash_color_cyan: "$'\e[1;36m'"
config_bash_color_white: "$'\e[1;37m'"

# establish termcap choices
# replace any of the choices below with your choices from the
# variable above.
# mb=Blinking color
# md=Bold color
# us=Underline
# me=End special formatting
# so=Stand out color
config_bash_reset_default: "$'\e[0m'"
config_bash_mb_choice: "{{ config_bash_color_blue }}"
config_bash_md_choice: "{{ config_bash_color_blue }}"
config_bash_me_choice: "{{ config_bash_reset_default }}"
config_bash_so_choice: "{{ config_bash_color_blue }}"
config_bash_se_choice: "{{ config_bash_reset_default }}"
config_bash_us_choice: "{{ config_bash_color_purple }}"
config_bash_ue_choice: "{{ config_bash_reset_default }}"

config_bash_bashrc_termcap_colors:
  - line: "export LESS_TERMCAP_mb={{ config_bash_mb_choice }}"
    regex: "TERMCAP_mb="
  - line: "export LESS_TERMCAP_md=={{ config_bash_md_choice }}"
    regex: "TERMCAP_md="
  - line: "export LESS_TERMCAP_me={{ config_bash_me_choice }}"
    regex: "TERMCAP_me="
  - line: "export LESS_TERMCAP_so={{ config_bash_so_choice }}"
    regex: "TERMCAP so="
  - line: "export LESS_TERMCAP_se={{ config_bash_se_choice }}"
    regex: "TERMCAP_se="
  - line: "export LESS_TERMCAP_us={{ config_bash_us_choice }}"
    regex: "TERMCAP_us="
  - line: "export LESS_TERMCAP_ue={{ config_bash_ue_choice }}"
    regex: "TERMCAP_uu="

Dependencies
------------

None

Example Playbook
----------------

License
-------

BSD

Author Information
------------------


