# Py3Xadmin

python版本：3.9.9

Django版本：2.2

importexport.py改动：

#/ from import_export.admin import DEFAULT_FORMATS, SKIP_ADMIN_LOG, TMP_STORAGE_CLASS

from import_export.formats.base_formats import DEFAULT_FORMATS

from import_export.admin import ImportMixin, ImportExportMixinBase


   def get_skip_admin_log(self):
   
    if self.skip_admin_log is None:
    
        return ImportMixin().get_skip_admin_log()
        
    else:
    
        return self.skip_admin_log


def get_tmp_storage_class(self):

    if self.tmp_storage_class is None:
    
        return ImportMixin().get_tmp_storage_class()
        
    else:
    
        return self.tmp_storage_class
