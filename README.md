# Group inheritance
#
# Any inherited groups prefixed with a g: are global groups
# and are inherited from the GlobalGroups.yml.
#
# Groups without the g: prefix are groups local to this world
# and are defined in the this groups.yml file.
#
# Local group inheritances define your promotion tree when using 'manpromote/mandemote'

groups:
  default:
    default: true
    permissions:
    - essentials.suicide
    - essentials.spawn
    - essentials.sethome
    - essentials.sethome.multiple
    - essentials.sethome.multiple.default
    - essentials.home
    - essentials.delhome
    - essentials.balance
    - essentials.help
    - essentials.pay
    - essentials.tpa
    - essentials.tpaccept
    - essentials.tpdeny
    - essentials.msg
    - essentials.reply
    - essentials.warp
    - essentials.warp.list
    - essentials.warps.shop
    - essentials.kit
    inheritance:
    info:
      prefix: '&f[&4Member&f]&f'
      build: true
      suffix: '&f'
  farmer:
    default: false
    permissions:
    - essentials.sethome.multiple
    - essentials.sethome.multiple.farmer
    - essentials.kit
    - essentials.kit.Farmer
    inheritance:
    - default
    info:
      prefix: '&f[&6Farmer&f]&f'
      build: true
      suffix: '&f'
  builder:
    default: false
    permissions:
    - essentials.sethome.multiple
    - essentials.sethome.multiple.builder
    - essentials.kit
    - essentials.kit.Builder
    inheritance:
    - default
    - farmer
    info:
      prefix: '&f[&cBuilder&f]'
      build: true
      suffix: '&f'
  knight:
    default: false
    permissions:
    - essentials.sethome.multiple
    - essentials.sethome.multiple.knight
    - essentials.kit
    - essentials.kit.Knight
    inheritance:
    - default
    - farmer
    - builder
    info:
      prefix: '&f[&9Knight&f]'
      build: true
      suffix: '&f'
  king:
    default: false
    permissions:
    - essentials.sethome.multiple
    - essentials.sethome.multiple.king
    - essentials.kit
    - essentials.kit.King
    - nv.use
    inheritance:
    - default
    - farmer
    - builder
    - knight
    info:
      prefix: '&f[&eKnight&f]'
      build: true
      suffix: '&f'
  l5:
    default: false
    permissions:
    - '*'
    - -vanish.*
    inheritance:
    - admin
    info:
      prefix: '&6&l[&a&lL5 Staff&6&l]'
      build: true
      suffix: ''
