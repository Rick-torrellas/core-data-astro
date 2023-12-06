<time>2023-11-21T12:00:12</time>
<main>
<header>
<h1>
    init
</h1>
</header>
<section>
    <p>
        Este es un archivo muy importante a la hora de crear modulos, sobre todo cuando se usar pip.
    </p>
    <p>
        Le indica a python que es un modulo, y tambien sus partes, para que despues pueda ser consumudo apropiadamente.
    </p>
    <p>
        tanto en la raiz del proyecto, como cada uno de sus submodulos, tienen que tener un archivo __init__.
    </p>
    <p>
        <b>
            Nota:
        </b> Tambien es importante crear un archivo con el nombre del submodulo, e importar todo ahi.
    </p>
    <div>
        <h2>
            Ejemplo de __init__
        </h2>
        <p>
            Estructura
        </p>
        <pre>
            <p>
                /core-scripts
                    __init__.py
                    fileSystem_files/
                        __init__.py
                        fileSystem_files.py
                        check_extension.py
                        get_extension.py
                        create_yaml.py
            </p>
        </pre>
        <p>
           <b> core-scripts/__init__.py</b>
        </p>
        <pre><code>
            from .fileSystem_files import fileSystem_files

            def name_main(name):
                """
                Verifica si el script fue ejecutado localmente o fue importado.
                """
                if name == "__main__":
                    return True
                return False
        </code></pre>
        <p><b>
            fileSystem_files/__init__.py
        </b></p>
        <pre><code>
            from .fileSystem_files import *
        </code></pre>
        <p><b>
            fileSystem_files/fileSystem_files.py
        </b></p>
        <pre><code>
            from .check_extension import check_extension
            from .get_extension import get_extension
            from .create_yaml import create_yaml
        </code></pre>
    </div>
</section>
</main>