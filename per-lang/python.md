# Python

## Best practises

### Code style

_PEP_ stands for a _Python Enhancement Proposal_. [PEP8](https://www.python.org/dev/peps/pep-0008/) is a coding style guide, setting out coding conventions for: naming, comments, whitespaces, code lay-out and so on.

### Checkers & linters

<table>
  <thead>
    <tr>
      <th style="text-align:left">tool</th>
      <th style="text-align:left">what it does</th>
      <th style="text-align:left">played around</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><a href="https://www.pylint.org/">pylint</a>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>checks for errors,</li>
          <li>detects code smells,</li>
          <li>enforces coding standard (close to PEP8),</li>
          <li>gives overall mark for the code analysed,</li>
          <li>recommends suggestions about refactors.</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://pypi.org/project/pyflakes/">pyflakes</a>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>examines the files individually = faster than pylint, but limited in the
            checks,</li>
          <li>no style checking,</li>
          <li>checks for errors,</li>
          <li>&#x2753; code smells detection</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://pypi.org/project/flake8/">Flake8</a>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>incorporates different tools:
            <ul>
              <li><a href="https://pypi.org/project/pycodestyle/">pycodestyle</a> (PEP8 checks),</li>
              <li><a href="https://pypi.org/project/pyflakes/">pyflakes</a> (see above),</li>
              <li><a href="https://github.com/PyCQA/mccabe">McCabe complexity checker</a>.</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/hhatto/autopep8">autopep8</a>
      </td>
      <td style="text-align:left">uses pycodestyle to automatically conform to PEP8.</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/python/mypy">mypy</a>
      </td>
      <td style="text-align:left">optional static type checker</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>On integrations with vim see [here](https://notes.ugabuga.eu/vim#syntax-linters-checkers).

## Debugging

Short listing on debugging tools I tried to use. On integrations with vim see [here](https://notes.ugabuga.eu/vim#debugging).

{% hint style="warning" %}
Do any of the following have any limitation when it comes to debugging:

* frameworks and code involving browser requests,
* tests.
{% endhint %}

### PDB

{% embed url="https://docs.python.org/3/library/pdb.html" %}

Starting it:

* python console: `import pdb; pdb.run('afunction()')`
* shell: `python3 -m pdb somescript.py`
* from code: `import pdb; pdb.set_trace()`

Using it: [a simple session with pdb](https://realpython.com/python-debugging-pdb/).

Pdb itself is not inviting to use, the presentation without any color makes the lines blend into one another.

### PDBPP

{% embed url="https://pypi.org/project/pdbpp/" %}

A PDB on steroids – it provides syntax highlighting which is easier on the eyes and tab completion among other things. After installing through pip it is used as if it were PDB \(it is a drop-in replacement after all\).

`import pdb; pdb.pdb.set_trace()` to get to the old pdb. 

### PUDB

{% embed url="https://documen.tician.de/pudb/" %}

Starting it, similarly to PDB:

* python console or code: `import pudb; pu.db`
* shell: `pudb3 my-script.py` or`python3 -m pudb somescript.py`
* possibility to control debugger from a separate terminal as well as remote debugging \(telnet\).

Using it: [a screencast with a pudb session](https://vimeo.com/5255125).

Pudb is nice to work with, having a friendlier interface than pdb, displaying the source file and location by default and in consequence letting to set breakpoints in a quite comfortable manner. It uses [Urwid library](http://urwid.org/) for the interface, hence the U in the name. It would be nice to be able to do everything in the UI by vim motions.

### IPDB

{% embed url="https://pypi.org/project/ipdb/" %}

{% embed url="http://keflavich.github.io/blog/my-python-ipython-vim-debugging-workflow.html" %}

## Testing

### Pytest



## Frameworks

### Flask

