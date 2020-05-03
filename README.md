# EasyPermissionX
运行时权限的获取
EasyPermissionX是一个针对Android运行时权限获取的一个封装

# How to use

## first

dependencies{
....
   implementation 'com.easypermissionx.hyploo:easypermissionx:1.0.0'
....
}

## second

### 申请单个权限
 EasyPermissionX.request(this, android.Manifest.permission.CALL_PHONE) { allGranted,         deniedList ->
       if (allGranted) {
           Toast.makeText(this, "You granted $deniedList", Toast.LENGTH_SHORT).show()
                } else {
               Toast.makeText(this, "You denied $deniedList", Toast.LENGTH_SHORT).show()
                }
            }
 
 ### 申请多个权限
 EasyPermissionX.request(this, android.Manifest.permission.CALL_PHONE,
                                android.Manifest.permission.READ_CONTACTS) { allGranted,     deniedList ->
        if (allGranted) {
           Toast.makeText(this, "You granted $deniedList", Toast.LENGTH_SHORT).show()
                } else {
               Toast.makeText(this, "You denied $deniedList", Toast.LENGTH_SHORT).show()
                }
            }
