# rfwp_adaptacion_jet_plugin_addon

Modificacion del plugin  JetPlugins Dynamic Data Addon de Crocoblock
Para acceder a una lista de imagenes propias.

En base.php se ha añadido la opcion
'rf_array'  =>__( 'RF lista', 'jet-elements-dynamic-data' ),
y, en caso de que se solicite, se invoca a una funcion propiascase 'rf_array':
				$pproyecto = isset($_GET['proyecto']) ? esc_attr(esc_html($_GET['proyecto'])) : 0;
				$new_loop =  rf_get_fotos_proyecto($pproyecto);
				break;
que facilita una lista de fotos con la estructura 
 $resultado[] = [
                    'id' => $page->imgIdWordpress,
                    'url' => $page->imgUrl,
                ];

Ha sido necesario implementar el id de la imagen para Wordpress

